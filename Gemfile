# SPDX-License-Identifier: Apache-2.0

# frozen_string_literal: true

# Copyright 2019-2020 Joel E. Anderson
#
# Licensed under the Apache License, Version 2.0 (the "License");
# you may not use this file except in compliance with the License.
# You may obtain a copy of the License at
#
#     http://www.apache.org/licenses/LICENSE-2.0
#
# Unless required by applicable law or agreed to in writing, software
# distributed under the License is distributed on an "AS IS" BASIS,
# WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
# See the License for the specific language governing permissions and
# limitations under the License.

source 'https://rubygems.org'

gemspec

gem 'json', '>= 1.8', '<= 2.3'

group :development do
  gem 'rake', '>= 0.9.2'
  gem 'rdoc', '>= 6.0'
end

group :test do
  gem 'codecov', '>= 0.1.14', require: false
  # minitest at or above 5.12 cause problems with rbx 4
  gem 'minitest', '>= 5.9', '< 5.12'
  gem 'rubocop', '>= 0.69', require: false
  # using simplecov 0.18 causes the following problem with truffleruby:
  # lib/simplecov.rb:236:in `floor': wrong number of arguments (given 1,
  # expected 0) (ArgumentError)
  # see the following travis build for an example:
  # https://travis-ci.org/github/goatshriek/wrapture/jobs/679280059
  # this is due to a compatibility issue with truffleruby that will be fixed in
  # version 20.1.0, and the upper limit can be removed after that
  # see https://github.com/oracle/truffleruby/issues/1899 for a similar issue
  # with another project
  gem 'simplecov', '>= 0.16.1', '< 0.18', require: false
end
