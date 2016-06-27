To read data: pd.read_csv("data/navalny/navalny_inbox.csv", sep=";", encoding="utf-8")

Columns description:
* 'id': unique message id;
* 'date': date;
* 'from': sender;
* 'to': recepient (should be navalny@gmail.com most of the time);
* 'subject': subject;
* 'body': whole email body;
* 'text': body without history;
* 'X': preprocessed text -- to lowercase, question marks padded with spaces, all other punctiation deleted, stopwords deleted;
* 'X_ws': same as above, but stopwords are not deleted;
* 'label': indicates reply expectations of the sender: 
  * 0 - ignore;
  * 1 - accountable non-answer;
  * 2 - postponed reply;
  * 3 - immediate reply;
