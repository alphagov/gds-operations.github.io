require 'open-uri'

task default: :update_repo_data

task :update_repo_data do
  # FIXME: Use a +.json+ extension once https://github.com/jekyll/jekyll/pull/2369
  # is included in a Jekyll release
  repo_data_file = File.join(File.dirname(__FILE__), '_data/repos.yml')

  open(repo_data_file, 'wb') do |file|
      STDOUT.puts "Updating GitHub repository data in '#{repo_data_file}'..."
      file << open('https://api.github.com/orgs/gds-operations/repos').read
      STDOUT.puts "Done."
  end
end
