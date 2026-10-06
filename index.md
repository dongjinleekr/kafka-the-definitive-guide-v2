<article class="book-card">
  <figure class="book-card__cover">
    <img src="{{ '/images/kafka-2nd-ko-cover.jpg' | relative_url }}" alt="카프카 핵심 가이드 (개정증보판) 표지" width="500" height="652">
  </figure>
  <div class="book-card__body">
    <p class="book-card__eyebrow">개정증보판</p>
    <p class="book-card__title">카프카 핵심 가이드 (개정증보판)</p>
    <p class="book-card__subtitle">대규모 실시간 데이터와 스트림 처리</p>
    <p class="book-card__desc">카프카를 개발한 컨플루언트와 링크드인의 엔지니어들이 직접 저술한 카프카 환경 구축과 운영에 대한 핵심 실무서.</p>
    <nav class="book-card__actions" aria-label="도서 자료">
      <a class="book-card__action book-card__action--primary" href="{{ '/example/' | relative_url }}">예제 코드</a>
      <a class="book-card__action" href="{{ '/errata/' | relative_url }}">정오표</a>
    </nav>
    <dl class="book-card__meta">
      <dt>정오표</dt>
      <dd>최종 업데이트 2025.11.04</dd>
      <dt>출판사 소개</dt>
      <dd><a href="https://jpub.tistory.com/1405">제이펍 블로그</a> · <a href="https://blog.naver.com/jeipubmarketer/223072290210">네이버 블로그</a></dd>
    </dl>
    <nav class="book-card__actions" aria-label="구입처">
      <a class="book-card__action" href="https://www.aladin.co.kr/shop/wproduct.aspx?ISBN=K102832629">알라딘</a>
      <a class="book-card__action" href="https://product.kyobobook.co.kr/detail/S000201464167">교보문고</a>
      <a class="book-card__action" href="http://www.yes24.com/Product/Goods/118397432">YES24</a>
    </nav>
  </div>
</article>

{% assign topic_updates = site.posts | where: "update_type", "topic" %}
{% include update-section.html section_id="topic-updates" title="관련 주제 업데이트" updates=topic_updates empty_text="관련 주제 업데이트를 준비하고 있습니다." archive_url="/topic-updates/" %}

{% assign other_updates = site.posts | where: "update_type", "other" %}
{% include update-section.html section_id="other-updates" title="기타 업데이트" updates=other_updates empty_text="기타 업데이트를 준비하고 있습니다." archive_url="/other-updates/" %}

<aside class="homepage-section" aria-labelledby="related-title">
  <h2 id="related-title" class="homepage-section__title">연관 서적</h2>
  <ul class="related-books">
    <li>
      <a class="related-book" href="https://dongjinleekr.github.io/apache-iceberg-the-definitive-guide/">
        <img class="related-book__cover" src="{{ '/images/apache-iceberg-ko-cover.jpg' | relative_url }}" alt="" width="500" height="652">
        <span class="related-book__text">
          <span class="related-book__title">아파치 아이스버그 완벽 가이드</span>
        </span>
      </a>
    </li>
  </ul>
</aside>
