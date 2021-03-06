# Changelog
All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [Unreleased]

## [2.4.1] - 2020-03-09
### Changed
- Use Collection.estimated_document_count() (which is a metadata query) instead
  of Collection.count_documents() (which is a full collection scan) in
  CatalogQuery ctor. The latter can be quite slow for large catalogs.

## [2.4.0] - 2020-03-02
### Added
- Experimental support for searches against LIGO-style GW contours

### Changed
- ra_key and dec_key are actually optional for sphere2d-indexed catalogs. For healpix-indexed catalogs, the key names are taken from meta.keys.
