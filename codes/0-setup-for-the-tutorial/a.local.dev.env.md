
# Local Development Environment

1. install [Node.js](https://nodejs.org/en/)

2. make a new project

```
npx create-react-app my-app

```

----

### code

> A component takes in parameters, called props (short for “properties”), and returns a hierarchy of views to display via the render method.

```
class Square extends React.Component {
	render() {
		return (
			<button className="square">
				{/* TODO */}
			</div>
		);
	}
}

class Board extends React.Component {
	renderSquare(i) {
		return <Square />;
	}
	
	render() {
		const status = 'Next player: X';
		
		return (
			<div>
				<div className="status">{status}</div>
				<div className="board-row">
				  {this.renderSquare(0)}
				  {this.renderSquare(1)}
				  {this.renderSquare(2)}
				</div>
				<div className="board-row">
				  {this.renderSquare(3)}
				  {this.renderSquare(4)}
				  {this.renderSquare(5)}
				</div>
				<div className="board-row">
				  {this.renderSquare(6)}
				  {this.renderSquare(7)}
				  {this.renderSquare(8)}
				</div>
			</div>
		);
	}
}

class Game extends React.Component {
	render() {
		return (
			<div className="game">
				<div className="game-board">
					<Board />
				</div>
				<div className>
			</div>
		);
	}
}
```
