from rest_framework.decorators import api_view
from rest_framework.response import Response

@api_view(['POST'])
def introduce_yourself(request):
    name = request.data.get('name', Mohamed Abdelmonem')
    occupation = request.data.get('occupation', 'Software Developer')
    interests = request.data.get('interests', ['Python', 'Django', 'Rest Framework'])

    introduction = f"Hello, my name is {name}. I am a {occupation} and my interests include {', '.join(interests)}."

    return Response({'introduction': introduction})
