# SQL-
Projects and Hands on Experiences involved in SQL


USE [DemoHealthCare]
 

Create FUNCTION [dbo].[CalculateTotal]  (@Price decimal(10,2),@Quantity int)

RETURNS decimal(10,2)


AS
BEGIN

	declare @Tax decimal(10,2)

	set @Tax=0.15

	RETURN @Price * @Quantity + @Tax


END
GO


Select [dbo].[CalculateTotal](15,5) 


Create procedure dbo.Test 
as 
Begin
		Select 'Orange','12','25',[dbo].[CalculateTotal](12,25) 

End 

Create procedure dbo.Admin 
as 
Begin
		Select 'Iphone','189','2',[dbo].[CalculateTotal](2,15) 

End 

exec dbo.Admin
exec dbo.Test 
                          
