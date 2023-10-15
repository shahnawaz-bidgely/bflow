# Bflow - bidgely official stack overflow

### Features
 - Users can create question
     - Question should have a heading, subheading, tags and content body.
     - Question will be having total answered count.
     - Question can be editable.
 - Users can upvote and down-vote on any answers.
 - Users can post answers on any question
   - Answer should have content body.
- Ability to filter question based on tags.
- Ability to search for question by heading
- Ability to sort question on feed by [date (default), tags]
- Add support for pagination when listing questions.
### module- Question

```json
 {
   "qId": 100,
   "heading": "Reco Model Killer not working",
   "subheding": "Killer not working",
   "description": "After taking survey some appliances killer is not working.",
   "answerCount": 5,
   "userId": "uuid-1",
   "tags": [
      "reco-model",
      "hybrid-model",
      "survey",
      "disagg"
   ],
   "answerList": [
      {},
      {},
      {}
   ]
}
```
### module- Answers

```json
 {
   "answerId": 1001,
   "qId": 100,
   "description": "Check the correct appliance",
   "userId": "uuid-5",
   "userName": "Shahnawaz",
   "upvote": 0,
   "downvote": 0
}
```

### API Endoints

#### Question
- Create question `POST /question/{userId}create/`
- Edit question `PUT /question/{userId}/edit/`

#### Answer
- create answer `POST /answer/create`
- On successfull answer submission increased answer count for particular question `PUT /answer/questin-count/{qid}/`

#### User
- upvote/downvote `PUT /user/answerId/upvote?true` 