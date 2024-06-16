# final-project-code
import random

def ladder_game(participants, outcomes):
    if len(participants) != len(outcomes):
        return "참가자 수와 상/벌 수가 일치해야 합니다."

    random.shuffle(outcomes)
    results = dict(zip(participants, outcomes))

    return results

# 예시 참가자 목록
participants = ["Team 1", "Team 2", "Team 3", "Team 4"]
# 예시 상/벌 목록
outcomes = ["love", "robot", "storm", "death"]

# 사다리타기 실행
results = ladder_game(participants, outcomes)

# 결과 출력
for participant, outcome in results.items():
    print(f"{participant} -> {outcome}")
