#Database tables: Users, courses, staff and programmes

**Users includes**
<ls>
	•	id	INT
	•	Courses_Shopping		INT (courses_id)
	•	Courses_taking		INT (courses_id)

**Courses**
	•	id			INT
	•	name	 		VARCHAR
	•	catalog_number	VARCHAR
	•	institute		VARCHAR
	•	credits			INT
	•	description		TEXT
	•	staff			INT (staff_id)
	•	programmes		INT (programme_id)
	•	restriction		TEXT

**Staff**
	•	id		INT
	•	name VARCHAR
	•	url		TEXT

**Programmes**
	•	id		INT
	•	name 	VARCHAR
	•	url		TEXT


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

Class Programmes 
	def show
		@programmes = Programme.find(params[:id])
	end


