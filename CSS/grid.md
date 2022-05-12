如陣列或表格般的格線，擁有行(columns)跟列(rows)，與各自的格線(column line)(row line)。
設定display: grid的父元素稱為格線容器(grid container)，裡面的子元素稱為格線單位(grid item)。

# Container設定
- grid-template-columns  設定行寬，auto為自動分配，屬性值有幾項則為設定此格線有幾行，如grid-template-columns: auto auto auto 代表為3×n的格線
- grid-template-rows  設定列高
- grid-auto-flow  排列方向，即Item排列的方向，預設為row，即橫向左到右，滿了再第二列。屬性值dense設定有空缺補位。
- grid-auto-rows  預設列高。當有多個屬性值時會呈現交互排列，如grid-auto-rows: 200px 300px; 換預設第一三五七列寬200px、第二四六八列寬300px。
- grid-auto-columns  預設行寬
- grid-template-areas  設定已命名區塊的位置。
  - 使用方法如grid-template-areas: "name name . ."; 代表name這個區塊佔據第一、二行，其他未命名佔據第三、四行，單點代表未命名區塊。
  - grid-template-areas: "name name . ." "name name . .";代表name這個區塊佔據第一、第二列的第一、二行，用空格區分下一列。
- grid-template  是grid-template-columns、grid-template-rows、grid-template-areas的簡寫，使用方式如下:
  - grid-template-rows: 200px 200px 300px; grid-template-columns: auto auto auto; 簡寫成grid-template:200px 200px 300px / auto auto auto; 用斜線區分，先寫row再寫column
  - grid-template-areas: "name name . ." "name name . ."; 使用grid-template則是不用改變，grid-template: "name name . ." "name name . .";
- grid  是grid-template與grid-auto合寫的簡寫，一樣先設定row再column並用斜線區隔。

- column-gap  設定各行間距。預設值0，即各行緊密相連。
- row-gap 設定各列間距
- gap  是column-gap及row-gap合寫的簡寫。先設定row再column，用空格區分。

- justify-items  Item在各自欄位中沿著Row軸的排列方式。預設值為stretch，其他值有start置前、end置尾、center置中
- align-items  Item在各自欄位中沿著Column軸的排列方式。
- place-items  是align-items與justify-items合寫的簡寫。先寫align-items再寫justify-items。
- justify-content  Item在Container中沿著Row軸的排列方式，與justify-items不同的是justify-items是在各自欄位的排列，justify-content是在整體Container的排列。預設值為stretch，其餘值除了有start、end、center外，還有
  - space-around  平均分配，兩側有空格，兩行間空格寬度是兩側空格的兩倍
  - space-between  平均分配，兩側無空格
  - space-evenly  平均分配，兩側有空格，兩行間空格寬度等同兩側空格
- align-content  Item在Container中沿著Column軸的排列方式
- place-content 是align-content與justify-content合寫的簡寫。先寫align-content再寫justify-content。


# Item設定
- grid-column 設定Item所在的直線(column line)範圍，如grid-column: 1/3 為佔據第1條線到第3條線的範圍，並合併儲存格。
- grid-row 同上，設定Item的橫線(row line)範圍
- grid-area  為Item所在的區塊命名，屬性值即名稱，不用引號。已命名區塊需要使用grid-template-areas這定位置。