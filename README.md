const password = document.getElementById('password')
const background = document.getElementById('background')

password.addEventListener('input', (e) => {
  const input = e.target.value
  const length = input.length
  const blurValue = 20 - length * 2
  background.style.filter = `blur(${blurValue}px)`
})https://images.unsplash.com/photo-1556745757-8d76bdb6984b* {
  box-sizing: border-box;
}

body {
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  height: 100vh;
  overflow: hidden;
  margin: 0;
}

.background {
  background: url('https://images.unsplash.com/photo-1556745757-8d76bdb6984b')
    no-repeat center center/cover;
  position: absolute;
  top: -20px;
  bottom: -20px;
  left: -20px;
  right: -20px;
  z-index: -1;
  filter: blur(20px);
}
