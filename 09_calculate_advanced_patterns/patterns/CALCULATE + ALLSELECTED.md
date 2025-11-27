(фільтри користувача, крім контексту візуалу)
Total Sales (Report Level Filters) =
CALCULATE (
    SUM ( Sales[Amount] ),
    ALLSELECTED ( Sales )
)
