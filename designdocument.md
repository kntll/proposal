<!DOCTYPE html>

<html>
<head></head>
<body>

**Database tables:** Users, courses, staff and programmes

**Users includes**

<table>
	<tr>
		<td> id </td> 	<td> INT </td>
	</tr>
	<tr> 
		<td>Courses-Shopping</td> <td> INT (courses_id) </td>
	</tr>
	<tr>	
		<td>Courses-taking </td><td>INT (courses-id)</td>
	</tr>

</table>

**Courses**
<table>
	<tr>
		<td> id</td><td>INT</td>
	</tr>
	<tr>	
		<td>name</td><td>VARCHAR</td>
	</tr>
	<tr>
		<td>catalog_number</td>	<td>VARCHAR</td>
	</tr>
	<tr>	
		<td>institute</td><td>VARCHAR</td>
	</tr>
	<tr>
		<td>credits</td><td>INT</td>
	</tr>
	<tr>
		<td>description</td><td>TEXT</td>
	</tr>
	<tr>
		<td>staff</td><td>INT (staff_id)</td>
	</tr>
	<tr>
		<td>programmes</td>	<td>INT (programme_id)</td>
	</tr>
	<tr>
		<td>restriction</td><td>TEXT</td>td>
	</tr>
</table>


**Staff**

<table>
	<tr>
		<td>id</td><td>INT</td>
	</tr>
	<tr>
		<td>name</td><td>VARCHAR</td>
	</tr>
	<tr>
		<td>url</td><td>TEXT</td>
	</tr>
</table>

**Programmes**

<table>
	<tr>
		<td>id</td><td>INT</td>
	</tr>
	<tr>
		<td>name</td><td>VARCHAR</td>
	</tr>
	<tr>
		<td>url</td><td>TEXT</td>
	</tr>
</table>


##Classes

class CourseController

	def save
		@course = Course.find(params[:id]
	end
	
	def destroy 
		@course = Course.find(params[:id])
		@course.destroy
	end
	
	def edit
		@course = Course.find(params[:id])
	end
	
	def index
		@course = Course.all
	end
	
	def show
		@course = Course.find([params[:id])	
	end

class CourseSearch

	def search
		@course = Couse.search(params[:id])
	end
	
	def index
		@courses = Course.all
	end
	
	def show
		@course = Course.find(params[:id])
  end
  
Class Staff

	def show
		@staff = Staff.find([params[:id])	
	end

class Programmes 

	def show
		@programmes = Programme.find(params[:id])
	end

	</body>
</html>
