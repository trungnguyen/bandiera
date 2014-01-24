# Bandiera

Bandiera is a simple, stand-alone feature flagging service that is not tied to
any existing web framework or language as all communication is via a simple
REST API.

# Bandiera Client Libraries

* **Ruby** - [https://github.com/nature/bandiera-client-ruby](https://github.com/nature/bandiera-client-ruby)
* **JavaScript** - _coming soon_
* **PHP** - _coming soon_

# Running a Bandiera Server

The Bandiera server is written in Ruby, so you're going to need to be able to
run a Ruby application within your organisation.

1. Clone this repo.
2. Run `bundle install --without development test`.
3. Create a `config/database.yml` file with your database connection details (use `config/database.yml.sample` as a guide).
4. Run `RACK_ENV=production bundle exec rake db:create db:migrate`.
5. Run `rackup -p 5000`

You'll now see the web interface sitting on [http://localhost:5000](http://localhost:5000),
and the API at [http://localhost:5000/api](http://localhost:5000/api).
Obviously in production, you'll want to run it via your favourite rack server
(i.e. [Puma][puma], [Unicorn][unicorn], [Thin][thin] or [Passenger][passenger]).

# Development

1. Fork this repo.
2. Run `bundle install`
3. Create a `config/database.yml` file with your database connection details (use `config/database.yml.sample` as a guide).
4. Run `bundle exec rake db:create db:migrate`.
5. Run `RACK_ENV=test bundle exec rake db:create db:migrate`.
6. Run `shotgun -p 5000`

You'll now see the web interface sitting on [http://localhost:5000](http://localhost:5000),
and the API at [http://localhost:5000/api](http://localhost:5000/api).

# License

[&copy; 2014, Nature Publishing Group](LICENSE.txt).

Bandiera is licensed under the [GNU General Public License 3.0][gpl].

[gpl]: http://www.gnu.org/licenses/gpl-3.0.html
[puma]: http://puma.io
[unicorn]: http://unicorn.bogomips.org
[thin]: http://code.macournoyer.com/thin/
[passenger]: https://www.phusionpassenger.com/

