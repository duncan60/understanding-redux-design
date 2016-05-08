# react-redux connect

Design pattern:
 - Higher-order function (高階函數)
 - Higher-order component (高階組建)

connect 重點：
 - merge 傳進來的 mapStateToProps, mapDispatchToProps 傳給 component 的 props
   * [code link](https://github.com/reactjs/react-redux/blob/master/src/components/connect.js#L10-L50)

 - 透過 context 取得 redux store，再由store.getState()取出 state
   * [code link](https://github.com/reactjs/react-redux/blob/master/src/components/connect.js#L83-L93)

 - componentDidMount  去 store.subscribe ，增聽 store state 的改變，componentWillUnmount 時，unsubscribe store
   * [code link](https://github.com/reactjs/react-redux/blob/master/src/components/connect.js#L197-L224)

 - 防止 component 不必要的更新
   * [code link](https://github.com/reactjs/react-redux/blob/master/src/components/connect.js#L274-L341)
   * [code link](https://github.com/reactjs/react-redux/blob/master/src/components/connect.js#L239-L263)

## 資源

[從 source code 來看 React-Redux 怎麼讓 Redux 跟 React 共舞](https://medium.com/@as790726/%E5%BE%9E-source-code-%E4%BE%86%E7%9C%8B-react-redux-%E6%80%8E%E9%BA%BC%E8%AE%93-redux-%E8%B7%9F-react-%E5%85%B1%E8%88%9E-a0777b99463a#.9lr1lfdib)

[JavaScript 中的高阶函数 (Higher-order functions)](https://happycoder.net/higher-order-functions-in-javascript/)

[高阶函数(Higher-order function)](https://jcouyang.gitbooks.io/functional-javascript/content/zh/!higher-order-function.html)