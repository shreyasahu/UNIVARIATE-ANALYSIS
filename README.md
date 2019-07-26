# UNIVARIATE-ANALYSIS
CONTAINS PLOTS TO DO UNIVARIATE ANALYSIS

FOR CREATING DISTPLOT OF CURRENT LOAN AMOUNT
    
    sns.distplot(df['Current Loan Amount'])
    
FOR CREATING PROBABILITY PLOT OF A COLUMN    
    
    stats.probplot(df['Bankruptcies'], dist="norm", plot=pylab)
    
FOR CREATING HIST PLOT OF A COLUMN    

    plt.hist(df['Bankruptcies'], bins=20)



    dfx=pd.DataFrame()
    dfx.fillna(0)
    dfx['Bankruptcies']=df["Bankruptcies"]
    sns.distplot(dfx)
    
    
    dfa = pd.DataFrame()
    dfa = dfa.fillna(0) # filling with with 0s 
    dfa[['Annual Income', 'Monthly Debt']] = df[['Annual Income', 'Monthly Debt']]
    dfa.plot.scatter('Annual Income','Monthly Debt')
    
    
 FOR CREATING BOXPLOT OF A COLUMN
    
    sns.boxplot(df['Current Loan Amount'],width=0.8, fliersize=5)
    sns.boxplot(df['Current Loan Amount'],width=0.8, fliersize=5)
    
    
    def number(df,col):
    plt.figure(figsize=(10,6))
    plt.subplot (1,2,1)
    plt.hist(df[col], bins=5)
    plt.subplot(1,2,2)
    sns.boxplot(df[col],width=0.8, fliersize=8)
    plt.show()
    
    number(df,'Number of Credit Problems')
    
FOR CREATING COUNT PLOT OF A COLUMN

    sns.countplot(df['Loan Status'])
    sns.countplot(df['Purpose'])
    plt.xticks(rotation=90)
    plt.show()


    
    
    
