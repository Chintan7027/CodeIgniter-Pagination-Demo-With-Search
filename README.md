# CodeIgniter-Pagination-Demo-With-Search
A complete demo to search the database and filter records with codeigniter pagination

#What is CodeIgniter

 CodeIgniter 2 Open Source PHP Framework (originally from EllisLab)- a toolkit - for people who build web sites using PHP. Its goal is to enable you to develop projects much faster than you could if you were writing code from scratch, by providing a rich set of libraries for commonly needed tasks, as well as a simple interface and logical structure to access these libraries. CodeIgniter lets you creatively focus on your project by minimizing the amount of code needed for a given task.

<b>Server Requirements</b>

PHP version 5.4 or newer is recommended.
This demo contains .htaccess to remove index.php. In order to take effect of these change your apcha is must enable with <i>mod_rewrite</i> <b>ON</b>

#Installation
<ol>
<li>You can import Cities.sql sample database dump in your database server. Here i have created <b>pagination</b> database in mysql, and 
<b>cities</b> table to access the sample records.</li>
<li>Clone the repository in your web directory and access the project using local web. </li>
</ol>

#Licence
Cities.sql database is Created by Haneef Puttur<br>
CodeIgniter 2.X version is access by understand and follow all the Terms and Conditions of 
<a href="https://github.com/bcit-ci/CodeIgniter/blob/develop/user_guide_src/source/license.rst" target="_blank">The MIT License (MIT) </a>

    #State of the art
    if (!empty($_GET['cityFilter'])) {
        $config["base_url"] = base_url('Listing/index?cityFilter=' . $_GET['cityFilter']);
    } else {
        $config["base_url"] = base_url('Listing/index?cityFilter=');
    }
    $config["total_rows"] = $totalRecords;
    $config["per_page"] = $limit;
    $config['use_page_numbers'] = TRUE;
    $config['page_query_string'] = TRUE;
    $config['enable_query_strings'] = TRUE;
    $config['num_links'] = 2;
    $config['cur_tag_open'] = '&nbsp;<li class="active"><a>';
    $config['cur_tag_close'] = '</a></li>';
    $config['next_link'] = 'Next';
    $config['prev_link'] = 'Previous';
    $this->pagination->initialize($config);
    $str_links = $this->pagination->create_links();
    $links = explode('&nbsp;', $str_links);
