- 👋 Hi, I’m @karimtmagdy
- 👀 I’m interested in ...
- 🌱 I’m currently learning ...
- 💞️ I’m looking to collaborate on ...
- 📫 How to reach me ...

<!---
karimtmagdy/karimtmagdy is a ✨ special ✨ repository because its `README.md` (this file) appears on your GitHub profile.
You can click the Preview link to take a look at your changes.
--->

from rest_framework.decorators import api_view
from rest_framework.response import Response

@api_view(['POST'])
def introduce_yourself(request):
    name = request.data.get('name', Mohamed Abdelmonem')
    occupation = request.data.get('occupation', 'Software Developer')
    interests = request.data.get('interests', ['Python', 'Django', 'Rest Framework'])

    introduction = f"Hello, my name is {name}. I am a {occupation} and my interests include {', '.join(interests)}."

    return Response({'introduction': introduction})
