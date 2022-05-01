![](Images/wallet.png)

# Crypto-Wallet-Web3

A project producing code that enables customers to send cryptocurrency payments to fintech professionals. From the perspective of a customer who is using the application to find a fintech professional and pay them for their work.

Contracted at a startup that is building a new and disruptive platform called Fintech Finder. Fintech Finder is an application that its customers can use to find fintech professionals from among a list of candidates, hire them, and pay them. As Fintech Finder’s lead developer, I have been tasked with integrating the Ethereum blockchain network into the application in order to enable your customers to instantly pay the fintech professionals whom they hire with cryptocurrency.
In this project, I have completed the code that enables customers to send cryptocurrency payments to fintech professionals. This app is an interface from the perspective of a Fintech Finder customer who is using the application to find a fintech professional and pay them for their work.

Language : Python
Web3, Streamlit library

Generated a new Ethereum account instance by using the mnemonic seed phrase provided by Ganache.


Displayed the account balance associated with the Ethereum account address.


Calculated the total value of an Ethereum transaction, including the gas estimate, that pays a Fintech Finder candidate for their work.


Allow for a customer to digitally sign a transaction that pays a Fintech Finder candidate, and send this transaction to the Ganache blockchain.


Allow confirmation and review of the transaction hash code associated with the validated blockchain transaction.

-Imported Ethereum Transaction Functions into the Fintech Finder Application
-Signed and Executed a Payment Transaction
-Inspected the Transaction on Ganache


 1: Imported Ethereum Transaction Functions into the Fintech Finder Application


Reviewed the code contained in the crypto_wallet.py script file. 
Note: Ethereum transaction functions include wallet, wallet.derive_acount, get_balance, fromWei, estimateGas, sendRawTransaction, and others—have now been incorporated into Python functions that allow to automate the process of accessing them.

Added mnemonic seed phrase (provided by Ganache) to the starter code’s .env file.


Within the Streamlit sidebar section of code, created a variable named account. Set this variable equal to a call on the generate_account function. This function  created the Fintech Finder customer’s (in this case, your) HD wallet and Ethereum account.


Within this same section of the fintech_finder.py file, I defined a new st.sidebar.write function that will display the balance of the customer’s account. Inside this function, I called the get_balance function and passed in the Ethereum account.address.
                                 
 2: Sign and Execute a Payment Transaction

Wrote the equation that calculates the candidate’s wage. This equation assessed the candidate’s hourly rate from the candidate database (candidate_database[person][3]) and then multiplied this hourly rate by the value of the hours variable. Saved this calculation’s output as a variable named wage.

Wrote the wage variable to the Streamlit sidebar by using st.sidebar.write.

Now that the application can calculate a candidate’s wage, I programmed the code that will allow a customer to send an Ethereum blockchain transaction that pays the hired candidate. 

Called the send_transaction function and pass it three parameters:

The wage value. This will be passed to the to Wei function to determine the wei value of the payment in the raw transaction.

Saved the transaction hash that the send_transaction function returns as a variable named transaction_hash, and had it display on the application’s web interface.

 3: Inspected the Transaction

Launched streamlit in gitbash using streamlit run fintech_finder.py.


The resulting webpage, allowed to select a candidate to hire from an appropriate drop-down menu. Then, allows to enter the number of hours that you would like to hire them for.

The app allows to Click the Send Transaction button to sign and send the transaction with your Ethereum account information and update in Ganache.

![](Images/FintechFinderjj.png)

![](Images/FintechFinderjjpg2.png)

A GIF is provided to show the live site in action. The program can be viewed by launching a local host and can be interacted once live. 
