# Account_java_code
import java.util.Scanner;
import java.util.Random;

public class Account {

	static String Surname;
	static String FirstName;
	static long AccountNumber;
	
	static String PhoneNumber;
	static String Email;
	
	static double Deposit;
	static double Withdrawal;
	static double CurrentBalance;
	static int TransactionCode;
	
	Account(){
		Surname = " ";
		FirstName = " ";
		
		PhoneNumber = " ";
		Email = " ";
		
		CurrentBalance = 0.00;
		Deposit = 0.00;
		Withdrawal = 0.00;
		}
	 void setSurname(String Sname){
		
		 Surname = Sname;
		
	}
	 
	 String getSurname(){
		 return Surname;
	 }
	 void setFirstName(String Fname){
			
		FirstName = Fname;
		
	}
	 
	 String getFirstName(){
		 return FirstName;
		 }
	 
	
	 
	 void setPhoneNumber(String Mobile){
			
		 PhoneNumber = Mobile;
		
	}
	 
	 String getPhoneNumber(){
		 return PhoneNumber;
	 }
	 
	 void setEmail(String Mail){
			
		 Email = Mail;
		
	}
	 
	 String getEmail(){
		 return Email;
	 }
	 
	 
	
	 
	 void setDeposit(double deposit){
			
		 Deposit = deposit;
		
	}
	 
	 double getDeposit(){
		 return Deposit;
	 }
	 
	 void setWithdrawal(double Withdraw){
			
		 Withdrawal = Withdraw;
		
	}
	 
	 double getWithdrawal(){
		 return Withdrawal;
	 }
	 


	 
	 
	

		

public static void main(String arg[]){
	
	Scanner Keyboard = new Scanner(System.in);
	
	System.out.println("Welcome to the ISSLNg Bank Account creation Portal. \n Please fill in the required details ");
	
	System.out.println("Surname");
	Surname = Keyboard.next();
	
	System.out.println("First Name");
	FirstName = Keyboard.next();
	
	System.out.println("Phone Number");
	PhoneNumber = Keyboard.next();
	
	System.out.println("Email");
	Email = Keyboard.next();
	
	System.out.println("Please input the amount you'd like to use to open your new account ");
	CurrentBalance =(double) Keyboard.nextDouble();
	
	
	
	
	Random AcctNum = new Random();
	AccountNumber = AcctNum.nextInt(1056789249) + 1000033333;
	
	System.out.println("Success!");
	System.out.println("Your Account has been succesfully created with the following Details: ");
	System.out.println("Account Name: " + Surname + " " + FirstName);
	System.out.println("Account Number: " + AccountNumber);
	System.out.println("Mobile: " + PhoneNumber);
	System.out.println("Email address: "+ Email);
	System.out.println("Current Account Balance: "+ "#" + CurrentBalance + "k");
	
	System.out.println("");
	
	System.out.println("You can now proceed to carry out transaction(s) on your Account");
	
	System.out.println("Please select one of the following options");
	System.out.println("For Withdrawal type 1 ");
	System.out.println("For Deposit type 2 ");
	System.out.println("For Account Balance type 3 ");
	System.out.println(" ");
	TransactionCode = Keyboard.nextInt();
	
	//withdrawal
	if (TransactionCode == 1){
		System.out.println("Please enter the amount you wish to withdraw");
		Withdrawal = (double) Keyboard.nextDouble();
		
		if (Withdrawal < CurrentBalance ){
			System.out.println("Insufficient Fund!");
			System.out.println("Session Ended");
			
		} else {
			System.out.println("Transaction Succesful! \n you have succefully withdrawn the sum of " + "#" + Withdrawal +"k" + "From your account");
			CurrentBalance = CurrentBalance - Withdrawal;
			System.out.println("Your current Account Balance is #" + CurrentBalance + "k");
			System.out.println("Session Ended");

		}
	
	//deposit	
	} else if (TransactionCode == 2){
		System.out.println("Please enter the amount you want to deposit");
		Deposit = (double) Keyboard.nextDouble();
		
		System.out.println("Transaction Successful");
		CurrentBalance = CurrentBalance + Deposit;
		System.out.println("Your current Account Balance is #" + CurrentBalance + "k");
		System.out.println("Session Ended");
		
	//Account Balance	
	} else if (TransactionCode == 3){
		System.out.println("Your current Account Balance is #" + CurrentBalance + "k");
		System.out.println("Session Ended");
		
	} else {
		System.out.println("Thank you for banking with us!");
	}
	
	
	
	
	
	
	
	
	
	
}










}
