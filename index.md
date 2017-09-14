---
layout: home-shape
---
<div class="container">
<div class="row">

<div class="col-md-6" markdown="1">

**What is OpenDataPlane?**

The ODP project has been established to produce an open-source, cross-platform set of application programming interfaces (APIs) for the networking data plane.

<br/>
<a href="https://git.linaro.org/lng/odp.git/blob_plain/HEAD:/doc/images/overview.svg">
    <img src="/assets/images/odp-overview.png" alt="OpenDataPlane Overview" class="img-responsive"/>
</a>

</div>
<div class="col-md-6">
    <div class="row">
        <div class="col-md-3">
            <a href="/about/">
                <img src="/assets/images/technical-overview.png" class="img-responsive" alt="OpenDataPlane Technical Overview Icon"/>
            </a>
        </div>
        <div class="col-md-9">
            <p>
                <strong>
                    Technical Overview
                </strong>
            </p>
            <p>Learn more about the goals of the ODP project including in-depth technical review and details in our presentation.</p>
        </div>
    </div>
    <hr>
    <div class="row">
        <div class="col-md-3">
            <a href="/about/">
                <img src="/assets/images/get-involved.png" class="img-responsive" alt="Get Involved with OpenDataPlane Icon"/>
            </a>
            <a href="/mailing-list/">
                <img src="/assets/images/mailing-list.png" class="img-responsive" alt="Mailing List OpenDataPlane Icon"/>
            </a>
        </div>
        <div class="col-md-9">
            <p>
                <strong>
                    Get Involved
                </strong>
            </p>

            <p>Please join us on on the mailing list or on Tuesday’s regular public meeting at 15:00 UTC at <a href="http://meetings.opendataplane.org/">meetings.opendataplane.org</a>.</p>
        </div>
    </div>
</div>
</div>

<div class="row">
    <div class="col-md-12">
        <hr>
    </div>
</div>

<div class="row">
    <div class="col-sm-6 odp-home-page-panel">
        <div class="row">   
            <div class="col-xs-3">
                <a href="https://www.opendataplane.org/opendataplane.org/odp-long-term-support-lts-release/">
                    <img src="/assets/images/monarchs-odp.png" class="img-responsive center-block" alt="OpenDataPlane Stable Version Icon"/>
                </a>
            </div>
            <div class="col-xs-9 text-center">
                <h3>OpenDataPlane</h3>
                <br/>
                <a href="https://www.opendataplane.org/opendataplane.org/odp-long-term-support-lts-release/" class="btn btn-default center-block">Long Term Stable</a>
            </div>
        </div>
    </div>
    <div class="col-sm-6 odp-home-page-panel">
            <div class="row">
                <div class="col-xs-3">
                    <a href="https://www.opendataplane.org/opendataplane.org/odp-long-term-support-lts-release/">
                        <img src="/assets/images/odp-contributing.png" class="img-responsive center-block" alt="Contribute to OpenDataPlane Icon"/>
                    </a>
                </div>
                <div class="col-xs-9">
                    <h3 class="text-center">Contribute to OpenDataPlane</h3>
                    <p>To contribute to ODP there is a contributor agreement:</p>
                    <ul>
                        <li><a href="/contributor/individual/">Individual</a></li>
                        <li><a href="/contributor/corporate/">Corporate</a></li>
                    </ul>
                </div>
            </div>
    </div>

    <hr>
    
</div>
</div>

<div class="row alt-row">
    <div class="container">
        <div class="row recent_posts">
            <h3 class="text-center">Latest Update</h3>
            {% for blog in site.posts limit: 3 %}
            <div class="blog_container col-md-4">
                <div class="recent_post">
                    <a href="{{blog.url}}">
                        <div class="recent_post_image">
                            <img class="recent_post_image" src="
                            {% if blog.featured_image %}
                                {% if site.using_assets %}
                                    {% asset_path '{{blog.featured_image}}' %}
                                {% else %}
                                    /assets{{blog.featured_image}}
                                {% endif %}
                            {% else %}
                                {% if site.using_assets %}
                                    {% asset_path 'placeholder.png' %}
                                {% else %}
                                    /assets/images/placeholder.png
                                {% endif %}
                            {% endif %}
                            "/>
                        </div>
                    </a>
                    <div class="recent_post_desc">
                        <a href="{{blog.url}}">
                            <h3 class="recent_post_title">{{blog.title | truncate: 40 | upcase}}</h3>
                        </a>
                        <small><em>{{blog.date | date: "%A, %B %-d, %Y" }}</em></small>
                    </div>
                    <div class="recent_post_more">
                        <a href="{{blog.url}}">> Read More</a>
                    </div>
                </div>
            </div>
            {% endfor %}
        </div>
        <a href="/news/" class="center-block more-news-button">More News</a>
    </div>
</div>
