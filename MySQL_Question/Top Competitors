SELECT h.hacker_id, h.name
FROM submissions s
     LEFT JOIN challenges c ON s.challenge_id = c.challenge_id
     LEFT JOIN difficulty d ON c.difficulty_level = d.difficulty_level
     LEFT JOIN hackers h ON s.hacker_id = h.hacker_id
WHERE s.score = d.score
GROUP BY h.hacker_id, h.name
HAVING COUNT(DISTINCT s.challenge_id) > 1
ORDER BY COUNT(DISTINCT s.challenge_id) DESC, h.hacker_id ASC
