-- Drop and create HelloWorldProcedure
IF OBJECT_ID('HelloWorldProcedure', 'P') IS NOT NULL
    DROP PROCEDURE HelloWorldProcedure;
GO

CREATE PROCEDURE HelloWorldProcedure
AS
BEGIN
    PRINT 'Hello World';
END;
GO

-- Execute HelloWorldProcedure
EXEC HelloWorldProcedure;
GO

-- Drop and create HelloWorldFunction
IF OBJECT_ID('dbo.HelloWorldFunction', 'FN') IS NOT NULL
    DROP FUNCTION dbo.HelloWorldFunction;
GO

CREATE FUNCTION dbo.HelloWorldFunction()
RETURNS VARCHAR(20)
AS
BEGIN
    RETURN 'Hello World';
END;
GO

-- Use HelloWorldFunction
SELECT dbo.HelloWorldFunction() AS regards;
GO

-- Drop and create Factorial procedure
IF OBJECT_ID('Factorial', 'P') IS NOT NULL
    DROP PROCEDURE Factorial;
GO

CREATE PROCEDURE Factorial
    @number INT,
    @result INT OUTPUT
AS
BEGIN
    DECLARE @i INT = 1;
    SET @result = 1;

    WHILE @i <= @number
    BEGIN
        SET @result = @result * @i;
        SET @i = @i + 1;
    END
END;
GO

-- Call the Factorial procedure
DECLARE @output INT;
EXEC Factorial @number = 5, @result = @output OUTPUT;
SELECT @output AS FactorialResult;
GO




-- Drop and create HelloWorldProcedure
IF OBJECT_ID('HelloWorldProcedure', 'P') IS NOT NULL
    DROP PROCEDURE HelloWorldProcedure;
GO

CREATE PROCEDURE HelloWorldProcedure
AS
BEGIN
    PRINT 'Hello World';
END;
GO

-- Execute HelloWorldProcedure
EXEC HelloWorldProcedure;
GO

-- Drop and create HelloWorldFunction
IF OBJECT_ID('dbo.HelloWorldFunction', 'FN') IS NOT NULL
    DROP FUNCTION dbo.HelloWorldFunction;
GO

CREATE FUNCTION dbo.HelloWorldFunction()
RETURNS VARCHAR(20)
AS
BEGIN
    RETURN 'Hello World';
END;
GO

-- Use HelloWorldFunction
SELECT dbo.HelloWorldFunction() AS regards;
GO

-- Drop and create Factorial procedure
IF OBJECT_ID('Factorial', 'P') IS NOT NULL
    DROP PROCEDURE Factorial;
GO

CREATE PROCEDURE Factorial
    @number INT,
    @result INT OUTPUT
AS
BEGIN
    DECLARE @i INT = 1;
    SET @result = 1;

    WHILE @i <= @number
    BEGIN
        SET @result = @result * @i;
        SET @i = @i + 1;
    END
END;
GO

-- Call the Factorial procedure
DECLARE @output INT;
EXEC Factorial @number = 5, @result = @output OUTPUT;
SELECT @output AS FactorialResult;
GO
