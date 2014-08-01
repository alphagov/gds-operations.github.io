require 'open-uri'

task default: :update_repo_data

task :update_repo_data do
  repo_data_file = File.join(File.dirname(__FILE__), '_data/repos.json')

  open(repo_data_file, 'wb') do |file|
      STDOUT.puts "Updating GitHub repository data in '#{repo_data_file}'..."
      file << open('https://api.github.com/orgs/gds-operations/repos').read
      STDOUT.puts "Done."
  end
end
