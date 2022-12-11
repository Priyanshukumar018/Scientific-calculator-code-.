# Scientific-calculator-code-.
How to make scientific calculator using python ?
class Calc():
	def __init__(self):
		self.total = 0
		self.current = ''
		self.input_value = True
		self.check_sum = False
		self.op = ''
		self.result = False

	def numberEnter(self, num):
		self.result = False
		firstnum = txtDisplay.get()
		secondnum = str(num)
		if self.input_value:
			self.current = secondnum
			self.input_value = False
		else:
			if secondnum == '.':
				if secondnum in firstnum:
					return
			self.current = firstnum+secondnum
		self.display(self.current)

	def sum_of_total(self):
		self.result = True
		self.current = float(self.current)
		if self.check_sum == True:
			self.valid_function()
		else:
			self.total = float(txtDisplay.get())

	def display(self, value):
		txtDisplay.delete(0, END)
		txtDisplay.insert(0, value)

	def valid_function(self):
		if self.op == "add":
			self.total += self.current
		if self.op == "sub":
			self.total -= self.current
		if self.op == "multi":
			self.total *= self.current
		if self.op == "divide":
			self.total /= self.current
		if self.op == "mod":
			self.total %= self.current
		self.input_value = True
		self.check_sum = False
		self.display(self.total)

	def operation(self, op):
		self.current = float(self.current)
		if self.check_sum:
			self.valid_function()
		elif not self.result:
			self.total = self.current
			self.input_value = True
		self.check_sum = True
		self.op = op
		self.result = False

	def Clear_Entry(self):
		self.result = False
		self.current = "0"
		self.display(0)
		self.input_value = True

	def All_Clear_Entry(self):
		self.Clear_Entry()
		self.total = 0

	def pi(self):
		self.result = False
		self.current = math.pi
		self.display(self.current)

	def tau(self):
		self.result = False
		self.current = math.tau
		self.display(self.current)

	def e(self):
		self.result = False
		self.current = math.e
		self.display(self.current)

	def mathPM(self):
		self.result = False
		self.current = -(float(txtDisplay.get()))
		self.display(self.current)

	def squared(self):
		self.result = False
		self.current = math.sqrt(float(txtDisplay.get()))
		self.display(self.current)

	def cos(self):
		self.result = False
		self.current = math.cos(math.radians(float(txtDisplay.get())))
		self.display(self.current)

	def cosh(self):
		self.result = False
		self.current = math.cosh(math.radians(float(txtDisplay.get())))
		self.display(self.current)

	def tan(self):
		self.result = False
		self.current = math.tan(math.radians(float(txtDisplay.get())))
		self.display(self.current)

	def tanh(self):
		self.result = False
		self.current = math.tanh(math.radians(float(txtDisplay.get())))
		self.display(self.current)

	def sin(self):
		self.result = False
		self.current = math.sin(math.radians(float(txtDisplay.get())))
		self.display(self.current)

	def sinh(self):
		self.result = False
		self.current = math.sinh(math.radians(float(txtDisplay.get())))
		self.display(self.current)

	def log(self):
		self.result = False
		self.current = math.log(float(txtDisplay.get()))
		self.display(self.current)

	def exp(self):
		self.result = False
		self.current = math.exp(float(txtDisplay.get()))
		self.display(self.current)

	def acosh(self):
		self.result = False
		self.current = math.acosh(float(txtDisplay.get()))
		self.display(self.current)

	def asinh(self):
		self.result = False
		self.current = math.asinh(float(txtDisplay.get()))
		self.display(self.current)

	def expm1(self):
		self.result = False
		self.current = math.expm1(float(txtDisplay.get()))
		self.display(self.current)

	def lgamma(self):
		self.result = False
		self.current = math.lgamma(float(txtDisplay.get()))
		self.display(self.current)

	def degrees(self):
		self.result = False
		self.current = math.degrees(float(txtDisplay.get()))
		self.display(self.current)

	def log2(self):
		self.result = False
		self.current = math.log2(float(txtDisplay.get()))
		self.display(self.current)

	def log10(self):
		self.result = False
		self.current = math.log10(float(txtDisplay.get()))
		self.display(self.current)

	def log1p(self):
		self.result = False
		self.current = math.log1p(float(txtDisplay.get()))
		self.display(self.current)


added_value = Calc()
