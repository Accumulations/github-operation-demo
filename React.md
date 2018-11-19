- componentWillMount(){  } 在组件即将被挂载到页面的时候自动执行

##生命周期函数
######组件挂载流程

componentWillMount  --> render -->  componentDidMount

```
componentWillMount() {xxx}--页面挂载之前执行
render() --组件渲染页面时执行，即页面挂载
componentDidMount()  -- 页面挂载之后执行
```

######updata--组件更新流程
当`props`或`states`发生改变时