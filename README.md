# Mui-Tree-Selects

使用 Mui Tree 搭配 checkbox 實現樹狀多選單

### install

**npm**

```
npm install mui-tree-selects
```

**yarn**

```
yarn add mui-tree-selects
```

### Props

| props         | 功能                                         |
| ------------- | -------------------------------------------- |
| iconDirection | 調整按鈕位置                                 |
| collapseIcon  | 收合時的 icon                                |
| expandIco     | 展開時的 icon                                |
| treeData      | 樹狀資料                                     |
| selectNode    | 已選擇的節點                                 |
| setSelectNode | 選取節點的 function (???)                    |
| iconReverse   | icon 顯示在後方，預設為 false => UIUX 怪怪的 |
| checkboxColor | checkbox 顏色，可自定義 => (border 可調整??) |
| expanded      | 可點擊的節點 (使用者自控) => 待補            |
| wrapperBorder | 最外層的 border 樣式                         |

> 有想加的 props 都歡迎發 PR

### treeData 格式

```ts
export type TreeData = {
  name: string
  id: string
  parent?: string
  children?: TreeData[]
}
```

### 使用

```ts
import React from 'react'

import { MuiTreeSelect } from 'mui-tree-selects'

import ExpandMoreIcon from '@mui/icons-material/ExpandMore'
import ChevronRightIcon from '@mui/icons-material/ChevronRight'

import data from './fakeData.json'

const App = () => {
  return (
    <MuiTreeSelect
      treeData={data}
      collapseIcon={<ExpandMoreIcon />}
      expandIcon={<ChevronRightIcon />}
      iconReverse={true}
    />
  )
}

export default App
```
