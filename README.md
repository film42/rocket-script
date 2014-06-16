Rocket Script
=============

Random idea I had about creating an s-expression syntax for ruby


Syntax Ideas
============

```clojure
(def person [x y z]
  (if (== x y) y z))
  
;; def person(x, y, z)
;;   if x == y
;;     y
;;   else
;;     z
;;   end
;; end

(module Company
  (class Employee
    
    (attr_accessor :name :age)
    
    (def to_s []
      (<< name age))
      
    (def transform [obj]
      (yield obj))))
      
;; module Company
;;   class Employee
;;     attr_accessor :name, :age
;;     
;;     def to_s
;;       name << age
;;     end
;;     
;;     def transform(obj)
;;       yield(obj)
;;     end
;;   end
;; end      
      
(def obtuse []
    (= e (new Company::Employee))
    (= e.name "janet")
    (e transform "this" 
      (do |e| (name e))))
    
;; def obtuse
;;   e = Company::Employee.new
;;   e.name = "janet"
;;   e.transform("this") { |e| e.name }
;; end
    
(obtuse) ;;=> janet

;; obtuse #=> janet
```

