# Chernovik
chernovik


@EntityGraph - ?????


 --------------------------------------------------------------------------------------------
 default void customize(@NotNull QuerydslBindings bindings, @NotNull QDocument document) {

        bindings.bind(document.qOnCheck).first((path, value) ->
                document.status.eq((DocumentStatusEnum.CHECKING)));


    public Page<DocumentDTO> getAllNonAuth(Predicate predicate, Pageable pageable, User user){
        final QDocument qDocument = QDocument.document;

        final BooleanBuilder builder = new BooleanBuilder(predicate);
        builder.and(qDocument.driver.isNotNull());
        return documentRepository.findAll(builder.getValue(),pageable).map(DocumentDTO::new);
    }


--------------------------------------------------------------------------------------------------


this.driver = new DriverDTO((document.getDriver()));
