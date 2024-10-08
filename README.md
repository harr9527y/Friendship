class Friendship:
    def __init__(self, person1, person2):
        self.person1 = person1
        self.person2 = person2
        self.trust_level = 0  # 信任度從0開始
        self.shared_experiences = []

    def share_experience(self, experience):
        self.shared_experiences.append(experience)
        self.trust_level += 1  # 隨著經歷增多，信任加深
        print(f"{self.person1} and {self.person2} shared an experience: {experience}. Trust level: {self.trust_level}")

    def help_each_other(self):
        if self.trust_level > 3:
            print(f"{self.person1} and {self.person2} are helping each other through tough times.")
        else:
            print(f"{self.person1} and {self.person2} are still getting to know each other.")

    def show_friendship(self):
        print(f"Friendship between {self.person1} and {self.person2}:")
        print(f"Trust level: {self.trust_level}")
        print(f"Shared experiences: {', '.join(self.shared_experiences)}")


# 創建兩個人的友情並模擬發展過程
friendship = Friendship("Alice", "Bob")
friendship.share_experience("Hiking trip")
friendship.share_experience("Graduation ceremony")
friendship.share_experience("Road trip")
friendship.help_each_other()
friendship.show_friendship()
# Friendship
