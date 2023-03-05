
.globl main


.text


main:
	li $t5,0
	li $t7,0
	li $s1,0
	li $s2,1
	j findlength

findlength:
	
	lb $t6,dest($t7)
	beq $t6,-127,presort
	addi $t7,$t7,1
	j findlength

presort:
	addi $t7,$t7,-1
	lb $zero,dest($t7)

sort:

	beq $s1,$t7,print
	lb $s3,dest($s1)
	lb $s4,dest($s2)
	bgt $s3,$s4,swap
	addi $s1,$s1,1
	addi $s2,$s2,1
	lb $t6,dest($s1)
	j sort

print:

	lb $t6,dest($t5)
	beq $t5,$t7,end
	addi $t5,$t5,1
	j print

swap:

	sb $s3,dest($s2)
	sb $s4,dest($s1)
	li $s1,0
	li $s2,1
	j sort
	
end:
 
	
	
.data
	dest: .byte 8,4,0,3,53,6,0,-127
	

