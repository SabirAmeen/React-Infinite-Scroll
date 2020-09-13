<h1>React-Infinite-Scroll 👋</h1>
<p>
  <img alt="Version" src="https://img.shields.io/badge/version-0.1.0-blue.svg?cacheSeconds=2592000" />
  <a href="#" target="_blank">
    <img alt="License: MIT" src="https://img.shields.io/badge/License-MIT-yellow.svg" />
  </a>
</p>

> <h1 align=&#34;center&#34;>An Infinite scroll component for React. 👋</h1>

### 🏠 [Homepage](https://github.com/SabirAmeen/React-Infinite-Scroll/blob/master/README.md)

## Install

```sh
npm install react-infinite-scroll --save
```

## Usage

A component that facilitates infinite scroll of a list of items.

```es6

// ScrollList.js
    import InfiniteScroll from "react-infinite-scroll";
    const ScrollList = () => {

        const renderContent = (data, index) => [
            // content to be rendered for each item
        ]

        return (
            props.dataList.map((data, index) => (
                renderContent(data, index)
            ))
        )
    }
    export default InfiniteScroll(ScrollList)
//

const ScrollComponent = ({dataList, offset, totalCount, fetchData scrollTarget }) => {
    return (
        <ScrollList
            dataList={dataList} // total dataList till now
            offset={offset} // offset of items
            totalCount={totalCount} // total count of items
            fetchData={fetchData} // function to be called on reaching end of list
            scrollTarget={scrollTarget}
        />
    )
}
```

## props

| name                           | type                 | description                                                                                                                                                                                                                                                                                                                                   |
| ------------------------------ | -------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **fetchData**                       | function             | a function which must be called after reaching the bottom. It must trigger some sort of action which fetches the next data. **The data is passed as `children` to the `InfiniteScroll` component and the data should contain previous items too.** e.g. _Initial data = [1, 2, 3]_ and then next load of data should be _[1, 2, 3, 4, 5, 6]_. |
| **offset**                    | number              | it tells the offset of the current list                                                                                                                                                                                                                                                                                                                                                                                                       |
| **totalCount**                 | number               | set the length of the data.This will unlock the subsequent calls to next.                                                                                                                                                                                                                                                                     |
| **scrollTarget**                     | node                 | The node to which the scroll events must be triggered.                                                                                                  

## Author

👤 **SabirAmeen**

- Github: [@SabirAmeen](https://github.com/SabirAmeen)

## Show your support

Give a ⭐️ if this project helped you!

---
