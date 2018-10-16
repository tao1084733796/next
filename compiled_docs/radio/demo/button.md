{"title":"按钮样式组件","meta":{"title":"按钮样式组件","description":"\n<p>使用 <code>RadioGroup</code> 渲染的组，通过设置 <code>shape=&quot;button&quot;</code> 可以让组件以按钮形式展示，同时可以通过 <code>size</code> 来控制组件大小。</p>\n","order":"4"},"codes":{"jsx":"import { Radio } from '@alifd/next';\n\nconst RadioGroup = Radio.Group;\n\nconst list = [\n    {\n        value: 'apple',\n        label: 'Apple',\n        disabled: false\n    }, {\n        value: 'pear',\n        label: 'Pear'\n    }, {\n        value: 'orange',\n        label: 'Orange',\n        disabled: true\n    }\n];\n\nclass ControlApp extends React.Component {\n    constructor(props) {\n        super(props);\n\n        this.state = {\n            value1: 'apple',\n            value2: ''\n        };\n\n        this.onNestChange = this.onNestChange.bind(this);\n        this.onNormalChange = this.onNormalChange.bind(this);\n    }\n\n    onNormalChange(value) {\n        this.setState({\n            value1: value\n        });\n    }\n\n    onNestChange(value) {\n        this.setState({\n            value2: value\n        });\n    }\n\n    render() {\n        return (\n            <div>\n                <h4>Small size</h4>\n                <RadioGroup dataSource={list} shape=\"button\" size=\"small\" value={this.state.value1} onChange={this.onNormalChange} />\n                <br/>\n                <br/>\n                <h4>Medium size (default)</h4>\n                <RadioGroup dataSource={list} shape=\"button\" size=\"medium\" value={this.state.value1} onChange={this.onNormalChange} />\n                <br/>\n                <br/>\n                <h4>Large size</h4>\n                <RadioGroup shape=\"button\" size=\"large\" value={this.state.value2} onChange={this.onNestChange}>\n                    <Radio id=\"banana\" value=\"banana\">Banana</Radio>\n                    <Radio id=\"watermelon\" value=\"watermelon\">Watermelon</Radio>\n                    <Radio id=\"peach\" value=\"peach\">Peach</Radio>\n                </RadioGroup>\n                <br/>\n                <br/>\n                <h4>Disabled and Selected-Disabled status</h4>\n                <RadioGroup shape=\"button\" value=\"banana\" onChange={this.onNestChange}>\n                    <Radio id=\"peach\" disabled value=\"peach\">Peach</Radio>\n                    <Radio id=\"banana\" disabled value=\"banana\">Banana</Radio>\n                </RadioGroup>\n\n            </div>\n        );\n    }\n}\n\nReactDOM.render(<ControlApp />, mountNode);\n"},"body":"\n\n````jsx\nimport { Radio } from '@alifd/next';\n\nconst RadioGroup = Radio.Group;\n\nconst list = [\n    {\n        value: 'apple',\n        label: 'Apple',\n        disabled: false\n    }, {\n        value: 'pear',\n        label: 'Pear'\n    }, {\n        value: 'orange',\n        label: 'Orange',\n        disabled: true\n    }\n];\n\nclass ControlApp extends React.Component {\n    constructor(props) {\n        super(props);\n\n        this.state = {\n            value1: 'apple',\n            value2: ''\n        };\n\n        this.onNestChange = this.onNestChange.bind(this);\n        this.onNormalChange = this.onNormalChange.bind(this);\n    }\n\n    onNormalChange(value) {\n        this.setState({\n            value1: value\n        });\n    }\n\n    onNestChange(value) {\n        this.setState({\n            value2: value\n        });\n    }\n\n    render() {\n        return (\n            <div>\n                <h4>Small size</h4>\n                <RadioGroup dataSource={list} shape=\"button\" size=\"small\" value={this.state.value1} onChange={this.onNormalChange} />\n                <br/>\n                <br/>\n                <h4>Medium size (default)</h4>\n                <RadioGroup dataSource={list} shape=\"button\" size=\"medium\" value={this.state.value1} onChange={this.onNormalChange} />\n                <br/>\n                <br/>\n                <h4>Large size</h4>\n                <RadioGroup shape=\"button\" size=\"large\" value={this.state.value2} onChange={this.onNestChange}>\n                    <Radio id=\"banana\" value=\"banana\">Banana</Radio>\n                    <Radio id=\"watermelon\" value=\"watermelon\">Watermelon</Radio>\n                    <Radio id=\"peach\" value=\"peach\">Peach</Radio>\n                </RadioGroup>\n                <br/>\n                <br/>\n                <h4>Disabled and Selected-Disabled status</h4>\n                <RadioGroup shape=\"button\" value=\"banana\" onChange={this.onNestChange}>\n                    <Radio id=\"peach\" disabled value=\"peach\">Peach</Radio>\n                    <Radio id=\"banana\" disabled value=\"banana\">Banana</Radio>\n                </RadioGroup>\n\n            </div>\n        );\n    }\n}\n\nReactDOM.render(<ControlApp />, mountNode);\n````","html":"<script>(function(){'use strict';\n\nvar _createClass = function () { function defineProperties(target, props) { for (var i = 0; i < props.length; i++) { var descriptor = props[i]; descriptor.enumerable = descriptor.enumerable || false; descriptor.configurable = true; if (\"value\" in descriptor) descriptor.writable = true; Object.defineProperty(target, descriptor.key, descriptor); } } return function (Constructor, protoProps, staticProps) { if (protoProps) defineProperties(Constructor.prototype, protoProps); if (staticProps) defineProperties(Constructor, staticProps); return Constructor; }; }();\n\nvar _next = require('@alifd/next');\n\nfunction _classCallCheck(instance, Constructor) { if (!(instance instanceof Constructor)) { throw new TypeError(\"Cannot call a class as a function\"); } }\n\nfunction _possibleConstructorReturn(self, call) { if (!self) { throw new ReferenceError(\"this hasn't been initialised - super() hasn't been called\"); } return call && (typeof call === \"object\" || typeof call === \"function\") ? call : self; }\n\nfunction _inherits(subClass, superClass) { if (typeof superClass !== \"function\" && superClass !== null) { throw new TypeError(\"Super expression must either be null or a function, not \" + typeof superClass); } subClass.prototype = Object.create(superClass && superClass.prototype, { constructor: { value: subClass, enumerable: false, writable: true, configurable: true } }); if (superClass) Object.setPrototypeOf ? Object.setPrototypeOf(subClass, superClass) : subClass.__proto__ = superClass; }\n\nvar RadioGroup = _next.Radio.Group;\n\nvar list = [{\n    value: 'apple',\n    label: 'Apple',\n    disabled: false\n}, {\n    value: 'pear',\n    label: 'Pear'\n}, {\n    value: 'orange',\n    label: 'Orange',\n    disabled: true\n}];\n\nvar ControlApp = function (_React$Component) {\n    _inherits(ControlApp, _React$Component);\n\n    function ControlApp(props) {\n        _classCallCheck(this, ControlApp);\n\n        var _this = _possibleConstructorReturn(this, (ControlApp.__proto__ || Object.getPrototypeOf(ControlApp)).call(this, props));\n\n        _this.state = {\n            value1: 'apple',\n            value2: ''\n        };\n\n        _this.onNestChange = _this.onNestChange.bind(_this);\n        _this.onNormalChange = _this.onNormalChange.bind(_this);\n        return _this;\n    }\n\n    _createClass(ControlApp, [{\n        key: 'onNormalChange',\n        value: function onNormalChange(value) {\n            this.setState({\n                value1: value\n            });\n        }\n    }, {\n        key: 'onNestChange',\n        value: function onNestChange(value) {\n            this.setState({\n                value2: value\n            });\n        }\n    }, {\n        key: 'render',\n        value: function render() {\n            return React.createElement(\n                'div',\n                null,\n                React.createElement(\n                    'h4',\n                    null,\n                    'Small size'\n                ),\n                React.createElement(RadioGroup, { dataSource: list, shape: 'button', size: 'small', value: this.state.value1, onChange: this.onNormalChange }),\n                React.createElement('br', null),\n                React.createElement('br', null),\n                React.createElement(\n                    'h4',\n                    null,\n                    'Medium size (default)'\n                ),\n                React.createElement(RadioGroup, { dataSource: list, shape: 'button', size: 'medium', value: this.state.value1, onChange: this.onNormalChange }),\n                React.createElement('br', null),\n                React.createElement('br', null),\n                React.createElement(\n                    'h4',\n                    null,\n                    'Large size'\n                ),\n                React.createElement(\n                    RadioGroup,\n                    { shape: 'button', size: 'large', value: this.state.value2, onChange: this.onNestChange },\n                    React.createElement(\n                        _next.Radio,\n                        { id: 'banana', value: 'banana' },\n                        'Banana'\n                    ),\n                    React.createElement(\n                        _next.Radio,\n                        { id: 'watermelon', value: 'watermelon' },\n                        'Watermelon'\n                    ),\n                    React.createElement(\n                        _next.Radio,\n                        { id: 'peach', value: 'peach' },\n                        'Peach'\n                    )\n                ),\n                React.createElement('br', null),\n                React.createElement('br', null),\n                React.createElement(\n                    'h4',\n                    null,\n                    'Disabled and Selected-Disabled status'\n                ),\n                React.createElement(\n                    RadioGroup,\n                    { shape: 'button', value: 'banana', onChange: this.onNestChange },\n                    React.createElement(\n                        _next.Radio,\n                        { id: 'peach', disabled: true, value: 'peach' },\n                        'Peach'\n                    ),\n                    React.createElement(\n                        _next.Radio,\n                        { id: 'banana', disabled: true, value: 'banana' },\n                        'Banana'\n                    )\n                )\n            );\n        }\n    }]);\n\n    return ControlApp;\n}(React.Component);\n\nReactDOM.render(React.createElement(ControlApp, null), mountNode);})()</script><div class=\"highlight\"><pre class=\"language-jsx\"><code class=\"language-jsx\"><span class=\"token keyword\">import</span> <span class=\"token punctuation\">{</span> Radio <span class=\"token punctuation\">}</span> <span class=\"token keyword\">from</span> <span class=\"token string\">'@alifd/next'</span><span class=\"token punctuation\">;</span>\n\n<span class=\"token keyword\">const</span> RadioGroup <span class=\"token operator\">=</span> Radio<span class=\"token punctuation\">.</span>Group<span class=\"token punctuation\">;</span>\n\n<span class=\"token keyword\">const</span> list <span class=\"token operator\">=</span> <span class=\"token punctuation\">[</span>\n    <span class=\"token punctuation\">{</span>\n        value<span class=\"token punctuation\">:</span> <span class=\"token string\">'apple'</span><span class=\"token punctuation\">,</span>\n        label<span class=\"token punctuation\">:</span> <span class=\"token string\">'Apple'</span><span class=\"token punctuation\">,</span>\n        disabled<span class=\"token punctuation\">:</span> <span class=\"token boolean\">false</span>\n    <span class=\"token punctuation\">}</span><span class=\"token punctuation\">,</span> <span class=\"token punctuation\">{</span>\n        value<span class=\"token punctuation\">:</span> <span class=\"token string\">'pear'</span><span class=\"token punctuation\">,</span>\n        label<span class=\"token punctuation\">:</span> <span class=\"token string\">'Pear'</span>\n    <span class=\"token punctuation\">}</span><span class=\"token punctuation\">,</span> <span class=\"token punctuation\">{</span>\n        value<span class=\"token punctuation\">:</span> <span class=\"token string\">'orange'</span><span class=\"token punctuation\">,</span>\n        label<span class=\"token punctuation\">:</span> <span class=\"token string\">'Orange'</span><span class=\"token punctuation\">,</span>\n        disabled<span class=\"token punctuation\">:</span> <span class=\"token boolean\">true</span>\n    <span class=\"token punctuation\">}</span>\n<span class=\"token punctuation\">]</span><span class=\"token punctuation\">;</span>\n\n<span class=\"token keyword\">class</span> <span class=\"token class-name\">ControlApp</span> <span class=\"token keyword\">extends</span> <span class=\"token class-name\">React<span class=\"token punctuation\">.</span>Component</span> <span class=\"token punctuation\">{</span>\n    <span class=\"token function\">constructor</span><span class=\"token punctuation\">(</span>props<span class=\"token punctuation\">)</span> <span class=\"token punctuation\">{</span>\n        <span class=\"token keyword\">super</span><span class=\"token punctuation\">(</span>props<span class=\"token punctuation\">)</span><span class=\"token punctuation\">;</span>\n\n        <span class=\"token keyword\">this</span><span class=\"token punctuation\">.</span>state <span class=\"token operator\">=</span> <span class=\"token punctuation\">{</span>\n            value1<span class=\"token punctuation\">:</span> <span class=\"token string\">'apple'</span><span class=\"token punctuation\">,</span>\n            value2<span class=\"token punctuation\">:</span> <span class=\"token string\">''</span>\n        <span class=\"token punctuation\">}</span><span class=\"token punctuation\">;</span>\n\n        <span class=\"token keyword\">this</span><span class=\"token punctuation\">.</span>onNestChange <span class=\"token operator\">=</span> <span class=\"token keyword\">this</span><span class=\"token punctuation\">.</span>onNestChange<span class=\"token punctuation\">.</span><span class=\"token function\">bind</span><span class=\"token punctuation\">(</span><span class=\"token keyword\">this</span><span class=\"token punctuation\">)</span><span class=\"token punctuation\">;</span>\n        <span class=\"token keyword\">this</span><span class=\"token punctuation\">.</span>onNormalChange <span class=\"token operator\">=</span> <span class=\"token keyword\">this</span><span class=\"token punctuation\">.</span>onNormalChange<span class=\"token punctuation\">.</span><span class=\"token function\">bind</span><span class=\"token punctuation\">(</span><span class=\"token keyword\">this</span><span class=\"token punctuation\">)</span><span class=\"token punctuation\">;</span>\n    <span class=\"token punctuation\">}</span>\n\n    <span class=\"token function\">onNormalChange</span><span class=\"token punctuation\">(</span>value<span class=\"token punctuation\">)</span> <span class=\"token punctuation\">{</span>\n        <span class=\"token keyword\">this</span><span class=\"token punctuation\">.</span><span class=\"token function\">setState</span><span class=\"token punctuation\">(</span><span class=\"token punctuation\">{</span>\n            value1<span class=\"token punctuation\">:</span> value\n        <span class=\"token punctuation\">}</span><span class=\"token punctuation\">)</span><span class=\"token punctuation\">;</span>\n    <span class=\"token punctuation\">}</span>\n\n    <span class=\"token function\">onNestChange</span><span class=\"token punctuation\">(</span>value<span class=\"token punctuation\">)</span> <span class=\"token punctuation\">{</span>\n        <span class=\"token keyword\">this</span><span class=\"token punctuation\">.</span><span class=\"token function\">setState</span><span class=\"token punctuation\">(</span><span class=\"token punctuation\">{</span>\n            value2<span class=\"token punctuation\">:</span> value\n        <span class=\"token punctuation\">}</span><span class=\"token punctuation\">)</span><span class=\"token punctuation\">;</span>\n    <span class=\"token punctuation\">}</span>\n\n    <span class=\"token function\">render</span><span class=\"token punctuation\">(</span><span class=\"token punctuation\">)</span> <span class=\"token punctuation\">{</span>\n        <span class=\"token keyword\">return</span> <span class=\"token punctuation\">(</span>\n            <span class=\"token tag\"><span class=\"token tag\"><span class=\"token punctuation\">&lt;</span>div</span><span class=\"token punctuation\">></span></span><span class=\"token plain-text\">\n                </span><span class=\"token tag\"><span class=\"token tag\"><span class=\"token punctuation\">&lt;</span>h4</span><span class=\"token punctuation\">></span></span><span class=\"token plain-text\">Small size</span><span class=\"token tag\"><span class=\"token tag\"><span class=\"token punctuation\">&lt;/</span>h4</span><span class=\"token punctuation\">></span></span><span class=\"token plain-text\">\n                </span><span class=\"token tag\"><span class=\"token tag\"><span class=\"token punctuation\">&lt;</span>RadioGroup</span> <span class=\"token attr-name\">dataSource</span><span class=\"token script language-javascript\"><span class=\"token script-punctuation punctuation\">=</span><span class=\"token punctuation\">{</span>list<span class=\"token punctuation\">}</span></span> <span class=\"token attr-name\">shape</span><span class=\"token attr-value\"><span class=\"token punctuation\">=</span><span class=\"token punctuation\">\"</span>button<span class=\"token punctuation\">\"</span></span> <span class=\"token attr-name\">size</span><span class=\"token attr-value\"><span class=\"token punctuation\">=</span><span class=\"token punctuation\">\"</span>small<span class=\"token punctuation\">\"</span></span> <span class=\"token attr-name\">value</span><span class=\"token script language-javascript\"><span class=\"token script-punctuation punctuation\">=</span><span class=\"token punctuation\">{</span><span class=\"token keyword\">this</span><span class=\"token punctuation\">.</span>state<span class=\"token punctuation\">.</span>value1<span class=\"token punctuation\">}</span></span> <span class=\"token attr-name\">onChange</span><span class=\"token script language-javascript\"><span class=\"token script-punctuation punctuation\">=</span><span class=\"token punctuation\">{</span><span class=\"token keyword\">this</span><span class=\"token punctuation\">.</span>onNormalChange<span class=\"token punctuation\">}</span></span> <span class=\"token punctuation\">/></span></span><span class=\"token plain-text\">\n                </span><span class=\"token tag\"><span class=\"token tag\"><span class=\"token punctuation\">&lt;</span>br</span><span class=\"token punctuation\">/></span></span><span class=\"token plain-text\">\n                </span><span class=\"token tag\"><span class=\"token tag\"><span class=\"token punctuation\">&lt;</span>br</span><span class=\"token punctuation\">/></span></span><span class=\"token plain-text\">\n                </span><span class=\"token tag\"><span class=\"token tag\"><span class=\"token punctuation\">&lt;</span>h4</span><span class=\"token punctuation\">></span></span><span class=\"token plain-text\">Medium size (default)</span><span class=\"token tag\"><span class=\"token tag\"><span class=\"token punctuation\">&lt;/</span>h4</span><span class=\"token punctuation\">></span></span><span class=\"token plain-text\">\n                </span><span class=\"token tag\"><span class=\"token tag\"><span class=\"token punctuation\">&lt;</span>RadioGroup</span> <span class=\"token attr-name\">dataSource</span><span class=\"token script language-javascript\"><span class=\"token script-punctuation punctuation\">=</span><span class=\"token punctuation\">{</span>list<span class=\"token punctuation\">}</span></span> <span class=\"token attr-name\">shape</span><span class=\"token attr-value\"><span class=\"token punctuation\">=</span><span class=\"token punctuation\">\"</span>button<span class=\"token punctuation\">\"</span></span> <span class=\"token attr-name\">size</span><span class=\"token attr-value\"><span class=\"token punctuation\">=</span><span class=\"token punctuation\">\"</span>medium<span class=\"token punctuation\">\"</span></span> <span class=\"token attr-name\">value</span><span class=\"token script language-javascript\"><span class=\"token script-punctuation punctuation\">=</span><span class=\"token punctuation\">{</span><span class=\"token keyword\">this</span><span class=\"token punctuation\">.</span>state<span class=\"token punctuation\">.</span>value1<span class=\"token punctuation\">}</span></span> <span class=\"token attr-name\">onChange</span><span class=\"token script language-javascript\"><span class=\"token script-punctuation punctuation\">=</span><span class=\"token punctuation\">{</span><span class=\"token keyword\">this</span><span class=\"token punctuation\">.</span>onNormalChange<span class=\"token punctuation\">}</span></span> <span class=\"token punctuation\">/></span></span><span class=\"token plain-text\">\n                </span><span class=\"token tag\"><span class=\"token tag\"><span class=\"token punctuation\">&lt;</span>br</span><span class=\"token punctuation\">/></span></span><span class=\"token plain-text\">\n                </span><span class=\"token tag\"><span class=\"token tag\"><span class=\"token punctuation\">&lt;</span>br</span><span class=\"token punctuation\">/></span></span><span class=\"token plain-text\">\n                </span><span class=\"token tag\"><span class=\"token tag\"><span class=\"token punctuation\">&lt;</span>h4</span><span class=\"token punctuation\">></span></span><span class=\"token plain-text\">Large size</span><span class=\"token tag\"><span class=\"token tag\"><span class=\"token punctuation\">&lt;/</span>h4</span><span class=\"token punctuation\">></span></span><span class=\"token plain-text\">\n                </span><span class=\"token tag\"><span class=\"token tag\"><span class=\"token punctuation\">&lt;</span>RadioGroup</span> <span class=\"token attr-name\">shape</span><span class=\"token attr-value\"><span class=\"token punctuation\">=</span><span class=\"token punctuation\">\"</span>button<span class=\"token punctuation\">\"</span></span> <span class=\"token attr-name\">size</span><span class=\"token attr-value\"><span class=\"token punctuation\">=</span><span class=\"token punctuation\">\"</span>large<span class=\"token punctuation\">\"</span></span> <span class=\"token attr-name\">value</span><span class=\"token script language-javascript\"><span class=\"token script-punctuation punctuation\">=</span><span class=\"token punctuation\">{</span><span class=\"token keyword\">this</span><span class=\"token punctuation\">.</span>state<span class=\"token punctuation\">.</span>value2<span class=\"token punctuation\">}</span></span> <span class=\"token attr-name\">onChange</span><span class=\"token script language-javascript\"><span class=\"token script-punctuation punctuation\">=</span><span class=\"token punctuation\">{</span><span class=\"token keyword\">this</span><span class=\"token punctuation\">.</span>onNestChange<span class=\"token punctuation\">}</span></span><span class=\"token punctuation\">></span></span><span class=\"token plain-text\">\n                    </span><span class=\"token tag\"><span class=\"token tag\"><span class=\"token punctuation\">&lt;</span>Radio</span> <span class=\"token attr-name\">id</span><span class=\"token attr-value\"><span class=\"token punctuation\">=</span><span class=\"token punctuation\">\"</span>banana<span class=\"token punctuation\">\"</span></span> <span class=\"token attr-name\">value</span><span class=\"token attr-value\"><span class=\"token punctuation\">=</span><span class=\"token punctuation\">\"</span>banana<span class=\"token punctuation\">\"</span></span><span class=\"token punctuation\">></span></span><span class=\"token plain-text\">Banana</span><span class=\"token tag\"><span class=\"token tag\"><span class=\"token punctuation\">&lt;/</span>Radio</span><span class=\"token punctuation\">></span></span><span class=\"token plain-text\">\n                    </span><span class=\"token tag\"><span class=\"token tag\"><span class=\"token punctuation\">&lt;</span>Radio</span> <span class=\"token attr-name\">id</span><span class=\"token attr-value\"><span class=\"token punctuation\">=</span><span class=\"token punctuation\">\"</span>watermelon<span class=\"token punctuation\">\"</span></span> <span class=\"token attr-name\">value</span><span class=\"token attr-value\"><span class=\"token punctuation\">=</span><span class=\"token punctuation\">\"</span>watermelon<span class=\"token punctuation\">\"</span></span><span class=\"token punctuation\">></span></span><span class=\"token plain-text\">Watermelon</span><span class=\"token tag\"><span class=\"token tag\"><span class=\"token punctuation\">&lt;/</span>Radio</span><span class=\"token punctuation\">></span></span><span class=\"token plain-text\">\n                    </span><span class=\"token tag\"><span class=\"token tag\"><span class=\"token punctuation\">&lt;</span>Radio</span> <span class=\"token attr-name\">id</span><span class=\"token attr-value\"><span class=\"token punctuation\">=</span><span class=\"token punctuation\">\"</span>peach<span class=\"token punctuation\">\"</span></span> <span class=\"token attr-name\">value</span><span class=\"token attr-value\"><span class=\"token punctuation\">=</span><span class=\"token punctuation\">\"</span>peach<span class=\"token punctuation\">\"</span></span><span class=\"token punctuation\">></span></span><span class=\"token plain-text\">Peach</span><span class=\"token tag\"><span class=\"token tag\"><span class=\"token punctuation\">&lt;/</span>Radio</span><span class=\"token punctuation\">></span></span><span class=\"token plain-text\">\n                </span><span class=\"token tag\"><span class=\"token tag\"><span class=\"token punctuation\">&lt;/</span>RadioGroup</span><span class=\"token punctuation\">></span></span><span class=\"token plain-text\">\n                </span><span class=\"token tag\"><span class=\"token tag\"><span class=\"token punctuation\">&lt;</span>br</span><span class=\"token punctuation\">/></span></span><span class=\"token plain-text\">\n                </span><span class=\"token tag\"><span class=\"token tag\"><span class=\"token punctuation\">&lt;</span>br</span><span class=\"token punctuation\">/></span></span><span class=\"token plain-text\">\n                </span><span class=\"token tag\"><span class=\"token tag\"><span class=\"token punctuation\">&lt;</span>h4</span><span class=\"token punctuation\">></span></span><span class=\"token plain-text\">Disabled and Selected-Disabled status</span><span class=\"token tag\"><span class=\"token tag\"><span class=\"token punctuation\">&lt;/</span>h4</span><span class=\"token punctuation\">></span></span><span class=\"token plain-text\">\n                </span><span class=\"token tag\"><span class=\"token tag\"><span class=\"token punctuation\">&lt;</span>RadioGroup</span> <span class=\"token attr-name\">shape</span><span class=\"token attr-value\"><span class=\"token punctuation\">=</span><span class=\"token punctuation\">\"</span>button<span class=\"token punctuation\">\"</span></span> <span class=\"token attr-name\">value</span><span class=\"token attr-value\"><span class=\"token punctuation\">=</span><span class=\"token punctuation\">\"</span>banana<span class=\"token punctuation\">\"</span></span> <span class=\"token attr-name\">onChange</span><span class=\"token script language-javascript\"><span class=\"token script-punctuation punctuation\">=</span><span class=\"token punctuation\">{</span><span class=\"token keyword\">this</span><span class=\"token punctuation\">.</span>onNestChange<span class=\"token punctuation\">}</span></span><span class=\"token punctuation\">></span></span><span class=\"token plain-text\">\n                    </span><span class=\"token tag\"><span class=\"token tag\"><span class=\"token punctuation\">&lt;</span>Radio</span> <span class=\"token attr-name\">id</span><span class=\"token attr-value\"><span class=\"token punctuation\">=</span><span class=\"token punctuation\">\"</span>peach<span class=\"token punctuation\">\"</span></span> <span class=\"token attr-name\">disabled</span> <span class=\"token attr-name\">value</span><span class=\"token attr-value\"><span class=\"token punctuation\">=</span><span class=\"token punctuation\">\"</span>peach<span class=\"token punctuation\">\"</span></span><span class=\"token punctuation\">></span></span><span class=\"token plain-text\">Peach</span><span class=\"token tag\"><span class=\"token tag\"><span class=\"token punctuation\">&lt;/</span>Radio</span><span class=\"token punctuation\">></span></span><span class=\"token plain-text\">\n                    </span><span class=\"token tag\"><span class=\"token tag\"><span class=\"token punctuation\">&lt;</span>Radio</span> <span class=\"token attr-name\">id</span><span class=\"token attr-value\"><span class=\"token punctuation\">=</span><span class=\"token punctuation\">\"</span>banana<span class=\"token punctuation\">\"</span></span> <span class=\"token attr-name\">disabled</span> <span class=\"token attr-name\">value</span><span class=\"token attr-value\"><span class=\"token punctuation\">=</span><span class=\"token punctuation\">\"</span>banana<span class=\"token punctuation\">\"</span></span><span class=\"token punctuation\">></span></span><span class=\"token plain-text\">Banana</span><span class=\"token tag\"><span class=\"token tag\"><span class=\"token punctuation\">&lt;/</span>Radio</span><span class=\"token punctuation\">></span></span><span class=\"token plain-text\">\n                </span><span class=\"token tag\"><span class=\"token tag\"><span class=\"token punctuation\">&lt;/</span>RadioGroup</span><span class=\"token punctuation\">></span></span><span class=\"token plain-text\">\n\n            </span><span class=\"token tag\"><span class=\"token tag\"><span class=\"token punctuation\">&lt;/</span>div</span><span class=\"token punctuation\">></span></span>\n        <span class=\"token punctuation\">)</span><span class=\"token punctuation\">;</span>\n    <span class=\"token punctuation\">}</span>\n<span class=\"token punctuation\">}</span>\n\nReactDOM<span class=\"token punctuation\">.</span><span class=\"token function\">render</span><span class=\"token punctuation\">(</span><span class=\"token tag\"><span class=\"token tag\"><span class=\"token punctuation\">&lt;</span>ControlApp</span> <span class=\"token punctuation\">/></span></span><span class=\"token punctuation\">,</span> mountNode<span class=\"token punctuation\">)</span><span class=\"token punctuation\">;</span></code></pre></div>"}