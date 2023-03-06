# Simple-Bank-Account-Creation

package Encapsulation;

public class Account {
	
	
	private String name ;
	private String bank ;
	private String type ;
	private String ifsc ;
	private long accno ;
	private double balance ;
	private int pin ;
	
	
	public String getName()
	{
		return name;
	}
	
	public String getBank()
	{
		return bank;
	}
	public String getIfsc()
	{
		return ifsc;
	}
	public void getPin(int acc, int old_pin, int new_pin)
	{
		if (acc==accno && old_pin==pin) {
			this.pin = new_pin;
			System.out.println("Pin Updated.");
			
		}
		else {
			System.out.println("Incorrect Credintials.");
		}
	}
	public String getType()
	{
		return type;
	}
	public void setBalance(int acc, int pass, double amount)
	{
		if (acc==accno && pass == pin) {
			System.out.println("Log in Success.");
			if (balance-amount>=1000) {
				System.out.println("Withdraw Successfully.");
				System.out.println(balance);
			}
			else
			{
				System.out.println("Insufficient Balance!");
			}
		}
	}
	public double getBalance(int acc , int pass)
	{
		if (acc== accno && pass ==pin) {
			return balance;
		}
		System.out.println("Incorrect Account number and pin!");
		return 0;
	}
	public long getAccno()
	{
		
		return accno;
	}
	
	

	Account()
	{}
	Account(String name, String bank, String type, String ifsc, long accno, double balance, int pin)
	{
		this.accno = accno;
		this.balance = balance ;	
		this.bank = bank;
		this.ifsc = ifsc;
		this.name = name;
		this.pin = pin;
		this.type = type;		
		
	}

}
	
