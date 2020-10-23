
Validation annotations that describe the method in which the field should be validated
    They are applied where the variable is declared
    @NotNull  (from javax.validation.constraints)
    @Size     (from javax.validation.constraints)
    @NotBlank (from javax.validation.constraints)
    @Pattern  (from javax.validation.constraints)
    @CreditCardNumber (from org.hibernate.validator.constraints)


@Valid (from javax.validation)
    Placed at parameter level in a function prototype declaration
    Tells jre to apply the validations specified in the class of the parameter
        before passing the parameter to the function so annotated.
        The function that has a parameter with this annotation, should have an
        other parameter as well of type Errors (org.springframework.validation.Errors)
