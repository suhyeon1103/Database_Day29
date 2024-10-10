### **1. INNER JOIN 문제**

**설명**: 여러 테이블을 조인하여 관련 데이터를 함께 가져오는 방법을 연습합니다.

**문제**:

다음의 테이블들이 있습니다:

- `students` (student_id, name)
- `enrollments` (student_id, course_id)
- `courses` (course_id, course_name)

각 학생이 수강 중인 과목의 이름을 모두 출력하는 쿼리를 작성하세요.

SELECT s.name, c.course_name
FROM students s
INNER JOIN enrollments e ON s.student_id = e.student_id
;

### **2. LEFT JOIN 문제**

**설명**: 왼쪽 테이블의 모든 행과 오른쪽 테이블의 일치하는 행을 가져오는 방법을 연습합니다.

**문제**:

다음의 테이블들이 있습니다:

- `employees` (employee_id, name, dept_id)
- `departments` (dept_id, dept_name)

모든 직원의 이름과 그들의 부서 이름을 가져오되, 부서가 없는 직원도 포함하여 부서가 없는 경우 부서 이름을 'None'으로 표시하는 쿼리를 작성하세요.

SELECT employees.name, departments.dept_name
FROM employees
LEFT JOIN departments
ON employees.dept_id = departments.dept_id;

### **3. RIGHT JOIN 문제**

**설명**: 오른쪽 테이블의 모든 행과 왼쪽 테이블의 일치하는 행을 가져오는 방법을 연습합니다.

**문제**:

다음의 테이블들이 있습니다:

- `products` (product_id, supplier_id, product_name)
- `suppliers` (supplier_id, supplier_name)

모든 공급업체의 이름과 그들이 제공하는 제품의 이름을 가져오되, 제품이 없는 공급업체도 포함하여 제품 이름을 'No Product'로 표시하는 쿼리를 작성하세요.

---

### **4. FULL OUTER JOIN 문제**

**설명**: 두 테이블의 모든 행을 가져와서 일치하는 데이터를 결합하는 방법을 연습합니다.

**문제**:

다음의 테이블들이 있습니다:

- `students` (student_id, name)
- `clubs` (club_id, club_name)
- `club_memberships` (student_id, club_id)

모든 학생과 모든 동아리를 가져오고, 학생이 어떤 동아리에 소속되어 있다면 그 동아리 이름을, 아니라면 NULL을 표시하는 쿼리를 작성하세요.

---

### **5. SELF JOIN 문제**

**설명**: 같은 테이블을 조인하여 계층적 또는 관련 데이터를 비교하는 방법을 연습합니다.

**문제**:

다음의 테이블이 있습니다:

- `employees` (employee_id, name, manager_id)

각 직원의 이름과 그들의 매니저 이름을 함께 출력하는 쿼리를 작성하세요. 매니저가 없는 경우 매니저 이름을 'No Manager'로 표시하세요.

---

### **6. GROUP BY 및 HAVING 문제**

**설명**: 데이터를 그룹화하고 그룹화된 데이터에 조건을 적용하는 방법을 연습합니다.

**문제**:

다음의 테이블이 있습니다:

- `sales` (sale_id, region, amount)

각 지역별 총 판매액을 계산하고, 총 판매액이 100,000 이상인 지역만 지역 이름과 총 판매액을 출력하는 쿼리를 작성하세요.

---

### **7. ORDER BY 및 LIMIT 문제**

**설명**: 데이터를 정렬하고 결과 수를 제한하는 방법을 연습합니다.

**문제**:

다음의 테이블이 있습니다:

- `products` (product_id, product_name, price)

가격이 가장 비싼 상위 5개의 제품 이름과 가격을 출력하는 쿼리를 작성하세요.

---

### **8. COUNT 함수 문제**

**설명**: 특정 조건에 맞는 행의 개수를 세는 방법을 연습합니다.

**문제**:

다음의 테이블이 있습니다:

- `orders` (order_id, customer_id, order_date)

각 고객별 주문 횟수를 계산하고, 주문 횟수가 5회 이상인 고객의 ID와 주문 횟수를 출력하는 쿼리를 작성하세요.

---

### **9. SUM 및 AVG 함수 문제**

**설명**: 합계와 평균을 계산하는 방법을 연습합니다.

**문제**:

다음의 테이블이 있습니다:

- `employees` (employee_id, name, department, salary)

각 부서별 총 급여 합계와 평균 급여를 계산하고 부서 이름, 총 합계, 평균 급여를 출력하는 쿼리를 작성하세요.

---

### **10. MAX 및 MIN 함수 문제**

**설명**: 최대값과 최소값을 찾는 방법을 연습합니다.

**문제**:

다음의 테이블이 있습니다:

- `products` (product_id, product_name, price)

전체 제품 중 가장 비싼 제품과 가장 저렴한 제품의 이름과 가격을 각각 출력하는 쿼리를 작성하세요.

---

### **11. 서브쿼리 문제**

**설명**: 서브쿼리를 사용하여 복잡한 조건을 적용하는 방법을 연습합니다.

**문제**:

다음의 테이블이 있습니다:

- `employees` (employee_id, name, salary)

직원들의 평균 급여보다 높은 급여를 받는 직원의 이름과 급여를 출력하는 쿼리를 작성하세요.

---

### **12. EXISTS 서브쿼리 문제**

**설명**: `EXISTS`를 사용하여 데이터의 존재 여부를 확인하는 방법을 연습합니다.

**문제**:

다음의 테이블이 있습니다:

- `customers` (customer_id, name)
- `orders` (order_id, customer_id, order_date)

주문을 한 적이 있는 고객의 이름과 ID를 출력하는 쿼리를 작성하세요.

---

### **13. UNION 문제**

**설명**: 여러 쿼리의 결과를 결합하여 하나의 결과로 만드는 방법을 연습합니다.

**문제**:

다음의 테이블이 있습니다:

- `current_students` (student_id, name)
- `alumni` (alumni_id, name)

현재 재학생과 졸업생의 이름을 모두 포함하는 명단을 중복 없이 출력하는 쿼리를 작성하세요.

---

### **14. INTERSECT 문제**

**설명**: 여러 쿼리의 공통 결과를 추출하는 방법을 연습합니다.

**문제**:

다음의 테이블이 있습니다:

- `customers` (customer_id, name)
- `subscribers` (customer_id, email)

회원이면서 뉴스레터 구독자인 고객의 이름을 출력하는 쿼리를 작성하세요.

---

### **15. EXCEPT 문제**

**설명**: 한 쿼리 결과에서 다른 쿼리 결과를 제외하는 방법을 연습합니다.

**문제**:

다음의 테이블이 있습니다:

- `students` (student_id, name)
- `graduates` (student_id, graduation_date)

졸업하지 않은 학생들의 이름을 출력하는 쿼리를 작성하세요.

---

### **16. 공통 테이블 표현식 (CTE) 문제**

**설명**: CTE를 사용하여 복잡한 쿼리를 가독성 있게 작성하는 방법을 연습합니다.

**문제**:

다음의 테이블이 있습니다:

- `employees` (employee_id, name, department, salary)

CTE를 사용하여 각 부서별 평균 급여를 계산하고, 평균 급여보다 낮은 급여를 받는 직원의 이름, 부서, 급여를 출력하는 쿼리를 작성하세요.

---

### **17. 재귀 CTE 문제**

**설명**: 재귀 CTE를 사용하여 계층적 데이터를 처리하는 방법을 연습합니다.

**문제**:

다음의 테이블이 있습니다:

- `categories` (category_id, category_name, parent_id)

재귀 CTE를 사용하여 모든 카테고리와 하위 카테고리를 계층적으로 표시하는 쿼리를 작성하세요.

---

### **18. 윈도우 함수 문제**

**설명**: 윈도우 함수를 사용하여 집계와 순위를 계산하는 방법을 연습합니다.

**문제**:

다음의 테이블이 있습니다:

- `sales` (sale_id, salesperson_id, amount, sale_date)

각 영업사원의 총 판매액과 전체 영업사원 중에서의 판매액 순위를 계산하여 영업사원 ID, 총 판매액, 순위를 출력하는 쿼리를 작성하세요.

---

### **19. 트랜잭션 문제**

**설명**: 트랜잭션을 사용하여 데이터 일관성을 유지하는 방법을 연습합니다.

**문제**:

다음의 테이블이 있습니다:

- `accounts` (account_id, customer_id, balance)

계좌 ID가 1인 계좌에서 계좌 ID가 2인 계좌로 500달러를 이체하는 트랜잭션을 작성하세요. 이체 중 오류가 발생하면 모든 작업이 취소되도록 해야 합니다.

---

### **20. 인덱스 및 성능 문제**

**설명**: 인덱스를 생성하여 쿼리 성능을 향상시키는 방법을 연습합니다.

**문제**:

다음의 테이블이 있습니다:

- `employees` (employee_id, name, department, hire_date)

`department`와 `hire_date` 컬럼에 복합 인덱스를 생성하는 쿼리를 작성하고, 특정 부서에서 최근에 고용된 직원 10명의 이름과 고용일을 빠르게 조회하는 쿼리를 작성하세요.
