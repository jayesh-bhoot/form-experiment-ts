submit_button -> toEntity(formFields) -> Errors? -> filterErrorsUntilCurrentSection() -> return { status: 'Fixing', fields, errors: {} }
inputChange -> if state "Fixing" -then-> toEntity(formFields) -> Errors? -> ...
							                 -else-> return {state: 'Filling', fields, errors: {}}
