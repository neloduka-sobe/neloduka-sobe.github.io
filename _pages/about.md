---
layout: about
title: whoami
permalink: /
subtitle: Average Machine Learning Enthusiast, Entrepreneur, Student, Lifelong Learner, Time Person of the Year 2006

profile:
  align: right
  image: prof_pic.jpg
  image_circular: true # crops the image to make it circular
  more_info:

news: false # includes a list of news items
selected_papers: false # includes a list of papers marked as "selected={true}"
social: true # includes social icons at the bottom of the page
---

```Python
class MachineLearningEngineer(HumanifiedLLM):
    def __init__(self):
        super().__init__()
        self.name, self.surname, , self.company, self.contact = [None * 4]
        self.skills = []

    def load_resume(self, resume_json):
        try:
            resume_data = json.loads(resume_json)
            self.name = resume_data.get('name')
            self.surname = resume_data.get('surname')
            self.job_title = resume_data.get('job_title')
            self.company = resume_data.get('company')
            self.email = resume_data.get('email')
            self.phone = resume_data.get('phone')
            self.skills = resume_data.get('skills', [])
        except json.JSONDecodeError as e:
            print(f"Error decoding JSON: {e}")

if __name__ == "__main__":
    me = MachineLearningEngineer()
    whoami = '''
    {
        "name": "Jane",
        "surname": "Smith",
        "job_title": "Data Scientist",
        "company": "Data Insights Inc.",
        "email": "",
        "phone": "",
        "skills": ["Python", "R", "SQL", "Machine Learning", "Data Visualization"]
    }
    '''
    me.load_resume(whoami)
```

