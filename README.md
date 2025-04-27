In this project let's build a **Covid19 Dashboard** 

### Set Up Instructions
<details>
<summary>Click to view</summary>

- Download dependencies by running `npm install`
- Start up the app using `npm start`
</details>

### Resources

<details>
<summary>Data fetch URLs</summary>

- Home Route:

  - Get stats of confirmed, active, recovered, deceased cases state wise (<u>sum of state wise data will give you national wise data</u>) :

    ```js
    'https://apis.ccbp.in/covid19-state-wise-data'

    ```

- State-Specific Route:

  - Get tested count, last updated date and stats of confirmed, active,recovered, deceased cases in specific states:

    ```js
    'https://apis.ccbp.in/covid19-state-wise-data'
    //(the response contains stats of all the States, you can use a state code (Ex:- "AP") to get specific state stats.)

    ```

  - Get districts (sort to show Top Districts):

    ```js
    'https://apis.ccbp.in/covid19-state-wise-data'
    //(the response contains stats of all the States, you can use a state code (Ex:- "AP") to get specific state stats.)

    ```

  - Sample Response for the API Url `https://apis.ccbp.in/covid19-state-wise-data`:

    ```json
    {
    "AP":{
      "districts":{
         "Anantapur":{
            "total":{
               "confirmed":157823,
               "deceased":1093,
               "recovered":156679,
               "tested":787085,
               "vaccinated1":2659813,
               "vaccinated2":1556657
            }
         }
      },
      "meta":{
         "date":"2021-10-28",
         "last_updated":"2021-10-28T20:20:18+05:30",
         "population":397000,
         "tested":{
            "date":"2021-10-27",
            "source":"https://dhs.andaman.gov.in/NewEvents/847.pdf"
         }
      },
      "total":{
         "confirmed":7651,
         "deceased":129,
         "recovered":7516,
         "tested":592748,
         "vaccinated1":293644,
         "vaccinated2":195689
      }
    }
      {...}
     }
    ```

  - Get timelines to show spread trends (use timelines data for rendering Bar chart, Line chart and other recharts by date-wise):

    ```js
    'https://apis.ccbp.in/covid19-timelines-data/AP'
    //(change state code in URL for other states)

    //(or)

    'https://apis.ccbp.in/covid19-timelines-data'
    //(the response contains stats of all the States, you can use a state code (Ex:- "AP") to get specific state stats.)

    ```

  - Sample Response

    ```json
    {
      "AN": {
        "dates": {
          "2021-09-09": {
            "total": {
              "confirmed": 7577,
              "deceased": 129,
              "recovered": 7441,
              "tested": 508157,
              "vaccinated1": 267126,
              "vaccinated2": 112124
            }
          },
          "2021-09-09": {...}
        }
      }
    }
    ```

- About Route:

  - Get faqs:

    ```js
    'https://apis.ccbp.in/covid19-faqs'

    ```

  - Sample Response

    ```json
    {
      "faq": [
        {
          "answer": "No.",
          "category": "General",
          "qno": "1",
          "question": "Are you official?"
        }
      ]
    }
    ```

    </details>
