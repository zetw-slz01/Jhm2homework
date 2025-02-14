# Jhm2homework
#Q1
#输入两个浮點數
price1 = float(input("Enter a price: ")) 
price2 = float(input("Enter another price: "))
# 比较两个浮點數的大小 
if price1 > price2:
    print("The first price is larger than the second one.") 
elif price1 < price2: 
 print("The first price is smaller than the second one.") 
else: 
 print("The prices are the same.")
#Q2-----------------------------------------------------------------------------------------------------------
 choice1 = input("Do you want some snacks? (yes/no): ") 
if choice1 == " no":
    print ("Good! Let's play games instead.") 
elif choice1 == "yes": 
    choice2 = input("Enter your choice (ice-cream / cookies / candies):") 
    if choice2 == "ice-cream":
       print ("Remember to wash your hands.") 
    elif choice2 == "cookies":
       print("Can you share with your friends?") 
    elif choice2 == "candies": 
        print("Don't eat too much.")
    else: 
        print("Invalid choice.")
#Q3-----------------------------------------------------------------------------------------------------------
#輸入加法口訣表的大小
size = int(input("Input Addition Table Size Smaller 10: ")) 
 #列印口訣表
print("Addition Table") 
print("-----------------------------------------------") 
 # 使用嵌套 for 循環生成加法口訣表  
for i in range(1, size + 1): 
 for j in range(1, size + 1): 
 # 計算
    sum_result = i + j 
    if sum_result < 10: 
     print(f"{i} + {j} ={sum_result} ", end="") 
    else: 
        print(f"{i} + {j} ={sum_result} ", end="") 
 # 换行 
 print()
 #Q4---------------------------------------------------------------------------------------------------------
 # 初級化變量 
height = [] 
num_students = 4 
 # 循環輸入四位同學的身高
while len(height) < num_students:
  try:
   heights = float(input(f"Input the height of a student {len(height) + 1} in cm: ")) 
   if heights < 0: 
     print("Height must be positive.") 
   elif heights > 200: 
    print("Height is greater than 200cm.")
   else:
    height.append(heights)
  except ValueError : 
   print(f"Invalid input: Please enter a number.") 
 # 輸入结束 
print("End of input.") 
 # 計算平均身高和最高身高 
if heights:
 average_heights = sum(height) / len(height)
max_heights = max(height) 
 # 顯示統計结果 
print(f"The average height of these students is {average_heights:.2f} cm.") 
print(f"The maximum height of these students is {max_heights:.2f} cm.")
#Q5-----------------------------------------------------------------------------------------------------------
import matplotlib.pyplot as plt
# 繪製長條圖
# 範例資料
products = ['jan', 'feb', 'mar', 'apr','may','jun','jul','aug','sep','oct','nov','dec']
revenue = [380, 400, 660, 800,900,1200,1600,2200,1500,1100,600,250]
# 繪製長條圖
plt.bar(products, revenue, color='green',width=0.5)
plt.title("Bar Chart of lce-cream Sales")  # 圖表標題
plt.xlabel("Month")         # X 軸標籤
plt.ylabel("Sales(in thousand dollars)") # Y 軸標籤
plt.show()
import matplotlib.pyplot as plt 
plt.rcParams['toolbar'] = 'None' # Disable the toolbar
#儲存圖表到檔案
plt.bar(products, revenue, color='green',width=0.5)
plt.title("Bar Chart of lce-cream Sales")
plt.xlabel("Month")
plt.ylabel("Sales(in thousand dollars)")
plt.legend()
plt.savefig("Bar_Chart_of_lce-cream_Sales.png")  # 儲存到檔案
print("圖表已儲存為Bar_Chart_of_lce-cream_Sales.png")
