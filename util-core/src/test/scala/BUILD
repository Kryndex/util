junit_tests(
  dependencies=[
    '3rdparty/jvm/junit:junit',
    '3rdparty/jvm/org/mockito:mockito-all',
    '3rdparty/jvm/org/scalacheck:scalacheck',
    '3rdparty/jvm/org/scalatest:scalatest',
    'util/util-core/src/main/scala:scala',
    'util/util-core/src/test/java:java',
  ],
  # fatal_warnings runs into an issue with scalatest/Future.isDone:
  #
  # [warn] ...: possible missing interpolator: detected interpolated identifier `$conforms`
  # [warn]     assert(future.close().isDone)
  # [warn]           ^
  #
  # At some point later, when we can enable `-Xlint:-warn-missing-interpolator`
  # for this target, we could try enabling this again.
  fatal_warnings=False,
  sources=rglobs('*.scala')
)
