GracityCave-MVC-Dynamic-Paging
===============================
<br>
<h2>What is this?</h2>
<b><i>GracityCave_MVCDynamicPaging</i></b> is a NugetPackage that enables you to easily add Paging functionality to IEnumerable/IQueryable in MVC.
<b><i>By Using this nuget you dont need to do any chnages in the controller. With just a HTmlHelper in view page everthing is done</i></b>
<br>

<h2>Installing and Using it....</h2>
    1. Search for GracityCave_MVCDynamicPaging in Nuget. nad install it.
    2. In your view page include AngularJS and bootstrap css.
         copy below code to view:
            <script src='http://code.angularjs.org/1.1.0/angular.min.js'></script>
            <link href="http://netdna.bootstrapcdn.com/twitter-bootstrap/2.1.1/css/bootstrap.no-icons.min.css"
                      rel="stylesheet">
            <link href="http://netdna.bootstrapcdn.com/font-awesome/2.0/css/font-awesome.css" rel="stylesheet">  
            
    3.Delete all auto generate code by visual studio in IEnumerable/IQueryable VIew. And add this line
                        
            @using GravityCave_MVCDynamicPaging
            @Html.MVCDyanmicPaging(Model)

<br>
<h2>Example </h2>
   <p> The view page looks like:</p>
    
        @model IEnumerable<MyModels.TestModel>
        @{
            ViewBag.Title = "Page Title";
        }
        @using GravityCave_MVCDynamicPaging
        <link href="http://netdna.bootstrapcdn.com/twitter-bootstrap/2.1.1/css/bootstrap.no-icons.min.css" rel="stylesheet">
        <link href="http://netdna.bootstrapcdn.com/font-awesome/2.0/css/font-awesome.css" rel="stylesheet">
        <script src='http://code.angularjs.org/1.1.0/angular.min.js'></script>
        @Html.MVCDyanmicPaging(Model)

    
    
<h2>Class Names to customise the css...</h2>
  <table>
      <tr>
            <th>HTML Element</th>
            <th>Class Name</th>
      </tr>
      <tr>
            <td>Select [used to select items per page]</td>
            <td>ItemsPerPageSelect</td>
      </tr>
      <tr>
            <td>Search Box</td>
            <td>inputSearch</td>
      </tr>
      <tr>
            <td>Table</td>
            <td>'ModelName'+DataGrid 
            [example: if modelname is 'TestModel'
                         class Name is 'TestModelDataGrid' ]</td>
      </tr>
      <tr>
            <td>UL [Paging buttons]</td>
            <td>paginationUL</td>
      </tr>
  </table>
