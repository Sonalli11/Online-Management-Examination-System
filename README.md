# Online-Management-Examination-System
&lt;%@PageLanguage=&quot;C#&quot;AutoEventWireup=&quot;true&quot;CodeFile=&quot;login.aspx.cs&quot;Inherits=&quot;login&quot;%&gt;
&lt;!DOCTYPEhtml&gt;
&lt;htmllang=&quot;en&quot;&gt;
&lt;head&gt;
&lt;metacharset=&quot;utf-8&quot;&gt;
&lt;metahttp-equiv=&quot;X-UA-Compatible&quot;content=&quot;IE=edge&quot;&gt;
&lt;metaname=&quot;viewport&quot;content=&quot;width=device-width, initial-scale=1, shrink-to-fit=no&quot;&gt;

51 | Page

&lt;metaname=&quot;description&quot;content=&quot;&quot;&gt;
&lt;metaname=&quot;author&quot;content=&quot;&quot;&gt;
&lt;title&gt;Login - Online exam sytem&lt;/title&gt;
&lt;!-- Bootstrap core CSS--&gt;
&lt;linkhref=&quot;assets/css/bootstrap.min.css&quot;rel=&quot;stylesheet&quot;&gt;
&lt;!-- Custom fonts for login--&gt;
&lt;linkhref=&quot;assets/css/custom.css&quot;rel=&quot;stylesheet&quot;&gt;
&lt;/head&gt;
&lt;bodyclass=&quot;bg-dark&quot;&gt;
&lt;divclass=&quot;container&quot;&gt;
&lt;divclass=&quot;card card-login mx-auto mt-5&quot;&gt;
&lt;divclass=&quot;card-header&quot;&gt;Student Login&lt;/div&gt;
&lt;divclass=&quot;card-body&quot;&gt;
&lt;formrunat=&quot;server&quot;id=&quot;formlogin&quot;&gt;
&lt;asp:PanelID=&quot;pnl_warning&quot;runat=&quot;server&quot;Visible=&quot;false&quot;&gt;
&lt;divclass=&quot;form-group card-header text-center&quot;&gt;
&lt;divclass=&quot;alert-danger&quot;&gt;
&lt;asp:LabelID=&quot;lbl_warning&quot;runat=&quot;server&quot;Text=&quot;Label&quot;CssClass=&quot;col-form-label text-center&quot;&gt;&lt;/asp:Label&gt;
&lt;/div&gt;
&lt;/div&gt;
&lt;/asp:Panel&gt;
&lt;divclass=&quot;form-group&quot;&gt;
&lt;labelfor=&quot;exampleInputEmail1&quot;&gt;Email address&lt;/label&gt;
&lt;asp:TextBoxID=&quot;txt_email&quot;runat=&quot;server&quot;CssClass=&quot;form-control&quot;placeholder=&quot;Enter
email&quot;TextMode=&quot;Email&quot;&gt;&lt;/asp:TextBox&gt;
&lt;asp:RequiredFieldValidatorID=&quot;rqr_emil&quot;runat=&quot;server&quot;ErrorMessage=&quot;Enter
email&quot;ControlToValidate=&quot;txt_email&quot;Display=&quot;Dynamic&quot;ForeColor=&quot;Red&quot;&gt;&lt;/asp:RequiredFieldValidator&gt;
&lt;asp:RegularExpressionValidatorID=&quot;rqrexpre_email&quot;runat=&quot;server&quot;ErrorMessage=&quot;Enter validate
email&quot;ValidationExpression=&quot;\w+([-+.&#39;]\w+)*@\w+([-.]\w+)*\.\w+([-
.]\w+)*&quot;ControlToValidate=&quot;txt_email&quot;Display=&quot;Dynamic&quot;ForeColor=&quot;Red&quot;&gt;&lt;/asp:RegularExpressionValidator&gt;
&lt;/div&gt;
&lt;divclass=&quot;form-group&quot;&gt;
&lt;divclass=&quot;form-row&quot;&gt;
&lt;divclass=&quot;col-md-6&quot;&gt;
&lt;labelfor=&quot;exampleInputPassword1&quot;&gt;Password&lt;/label&gt;
&lt;asp:TextBoxID=&quot;txt_pass&quot;runat=&quot;server&quot;CssClass=&quot;form-control&quot;placeholder=&quot;Enter
password&quot;TextMode=&quot;Password&quot;&gt;&lt;/asp:TextBox&gt;
&lt;asp:RequiredFieldValidatorID=&quot;rqr_pass&quot;runat=&quot;server&quot;ErrorMessage=&quot;Enter
password&quot;ControlToValidate=&quot;txt_pass&quot;Display=&quot;Dynamic&quot;ForeColor=&quot;Red&quot;&gt;&lt;/asp:RequiredFieldValidator&gt;
&lt;/div&gt;
&lt;divclass=&quot;col-md-6&quot;&gt;
&lt;labelfor=&quot;exampleConfirmPassword&quot;&gt;Confirm password&lt;/label&gt;
&lt;asp:TextBoxID=&quot;txt_repass&quot;runat=&quot;server&quot;CssClass=&quot;form-control&quot;placeholder=&quot;Re-type
password&quot;TextMode=&quot;Password&quot;&gt;&lt;/asp:TextBox&gt;
&lt;asp:CompareValidatorID=&quot;rqrcopm_pass&quot;runat=&quot;server&quot;ErrorMessage=&quot;Password do not
match&quot;ControlToValidate=&quot;txt_repass&quot;Display=&quot;Dynamic&quot;ForeColor=&quot;Red&quot;ControlToCompare=&quot;txt_pass&quot;&gt;&lt;/asp:
CompareValidator&gt;
&lt;/div&gt;
&lt;/div&gt;
&lt;/div&gt;
&lt;divclass=&quot;form-group&quot;&gt;
&lt;divclass=&quot;form-check&quot;&gt;
&lt;labelclass=&quot;form-check-label&quot;&gt;
&lt;asp:CheckBoxID=&quot;chk_remember&quot;runat=&quot;server&quot;CssClass=&quot;form-check-input remembermecustom&quot;/&gt;
Remember Password&lt;/label&gt;
&lt;/div&gt;

52 | Page

&lt;/div&gt;
&lt;asp:ButtonID=&quot;btn_login&quot;runat=&quot;server&quot;Text=&quot;Log In&quot;CssClass=&quot;btn btn-primary btn-
block&quot;OnClick=&quot;btn_login_Click&quot;/&gt;
&lt;divclass=&quot;text-center&quot;&gt;
&lt;aclass=&quot;d-block small mt-3&quot;href=&quot;register.aspx&quot;&gt;Register an Account&lt;/a&gt;
&lt;aclass=&quot;d-block small mt-3&quot;href=&quot;HomePage.aspx&quot;&gt;Go To Home Page&lt;/a&gt;
&lt;/div&gt;
&lt;/form&gt;
&lt;/div&gt;
&lt;/div&gt;
&lt;/div&gt;
&lt;/body&gt;
&lt;/html&gt;
 Login.aspx.cs
using System;
using System.Collections.Generic;
using System.Linq;
using System.Web;
using System.Web.UI;
using System.Web.UI.WebControls;
using System.Data.SqlClient;
using System.Data;
using System.Configuration;
publicpartialclasslogin : System.Web.UI.Page
{
protectedvoid Page_Load(object sender, EventArgs e)
{
}
string s = ConfigurationManager.ConnectionStrings[&quot;dbcs&quot;].ConnectionString;
//for login
protectedvoid btn_login_Click(object sender, EventArgs e)
{
if (Page.IsValid)
{using (SqlConnection con = new SqlConnection(s))
{
SqlCommand cmd = new SqlCommand(&quot;spUserslogin&quot;, con);
cmd.CommandType = CommandType.StoredProcedure;
cmd.Parameters.AddWithValue(&quot;@user_email&quot;, txt_email.Text);
cmd.Parameters.AddWithValue(&quot;@password&quot;, txt_pass.Text);
try
{
con.Open();
int value = (int)cmd.ExecuteScalar();
if (value == 1)
{
if (chk_remember.Checked)
{
HttpCookie user = new HttpCookie(&quot;user_cookies&quot;); //creating cookie object where user_cookies
is cookie name
user[&quot;Useremail&quot;] = txt_email.Text; // cookie content
user.Expires = DateTime.Now.AddYears(3); // give the time/duration of cookie
Response.Cookies.Add(user); // it gives the response in browser
}
else

53 | Page

{
Session[&quot;Useremail&quot;] = txt_email.Text;
}
Response.Redirect(&quot;index.aspx&quot;);
}
else
{
pnl_warning.Visible = true;
lbl_warning.Text = &quot;Use correct email and password&lt;/br&gt;&quot;;
}
}
catch (Exception ex)
{
pnl_warning.Visible = true;
lbl_warning.Text = &quot;Something went wrong! Contact your devloper &lt;/br&gt;&quot; + ex.Message;
}
}
}
else
{
pnl_warning.Visible = true;
lbl_warning.Text = &quot;Please fill all the requirements&quot;;
}
}
}
 Register.aspx
&lt;%@PageLanguage=&quot;C#&quot;AutoEventWireup=&quot;true&quot;CodeFile=&quot;register.aspx.cs&quot;Inherits=&quot;register&quot;%&gt;
&lt;!DOCTYPEhtml&gt;
&lt;htmllang=&quot;en&quot;&gt;
&lt;head&gt;
&lt;metacharset=&quot;utf-8&quot;&gt;
&lt;metahttp-equiv=&quot;X-UA-Compatible&quot;content=&quot;IE=edge&quot;&gt;
&lt;metaname=&quot;viewport&quot;content=&quot;width=device-width, initial-scale=1, shrink-to-fit=no&quot;&gt;
&lt;metaname=&quot;description&quot;content=&quot;&quot;&gt;
&lt;metaname=&quot;author&quot;content=&quot;&quot;&gt;
&lt;title&gt;Register - Online exam sytem&lt;/title&gt;
&lt;!-- Bootstrap core CSS--&gt;
&lt;linkhref=&quot;assets/css/bootstrap.min.css&quot;rel=&quot;stylesheet&quot;&gt;
&lt;!-- Custom styles for this register--&gt;
&lt;linkhref=&quot;assets/css/custom.css&quot;rel=&quot;stylesheet&quot;&gt;
&lt;/head&gt;
&lt;bodyclass=&quot;bg-dark&quot;&gt;
&lt;divclass=&quot;container&quot;&gt;
&lt;divclass=&quot;card card-register mx-auto mt-5&quot;&gt;
&lt;divclass=&quot;card-header&quot;&gt;Register an Account&lt;/div&gt;
&lt;divclass=&quot;card-body&quot;&gt;
&lt;formrunat=&quot;server&quot;id=&quot;formregister&quot;&gt;
&lt;asp:PanelID=&quot;pnl_warning&quot;runat=&quot;server&quot;Visible=&quot;false&quot;&gt;
&lt;divclass=&quot;form-group card-header text-center&quot;&gt;
&lt;divclass=&quot;alert-danger&quot;&gt;
&lt;asp:LabelID=&quot;lbl_warning&quot;runat=&quot;server&quot;Text=&quot;Label&quot;CssClass=&quot;col-form-label text-center&quot;&gt;&lt;/asp:Label&gt;
&lt;/div&gt;
&lt;/div&gt;
&lt;/asp:Panel&gt;

54 | Page

&lt;divclass=&quot;form-group&quot;&gt;
&lt;divclass=&quot;form-row&quot;&gt;
&lt;divclass=&quot;col-md-6&quot;&gt;
&lt;labelfor=&quot;exampleInputName&quot;&gt;First name&lt;/label&gt;
&lt;asp:TextBoxID=&quot;txt_fname&quot;runat=&quot;server&quot;CssClass=&quot;form-control&quot;placeholder=&quot;Enter first
name&quot;&gt;&lt;/asp:TextBox&gt;
&lt;asp:RequiredFieldValidatorID=&quot;rqr_name&quot;runat=&quot;server&quot;ErrorMessage=&quot;Enter first
name&quot;ControlToValidate=&quot;txt_fname&quot;Display=&quot;Dynamic&quot;ForeColor=&quot;Red&quot;&gt;&lt;/asp:RequiredFieldValidator&gt;
&lt;/div&gt;
&lt;divclass=&quot;col-md-6&quot;&gt;
&lt;labelfor=&quot;exampleInputLastName&quot;&gt;Last name&lt;/label&gt;
&lt;asp:TextBoxID=&quot;txt_lname&quot;runat=&quot;server&quot;CssClass=&quot;form-control&quot;placeholder=&quot;Enter last
name&quot;&gt;&lt;/asp:TextBox&gt;
&lt;asp:RequiredFieldValidatorID=&quot;rqr_lname&quot;runat=&quot;server&quot;ErrorMessage=&quot;Enter last
name&quot;ControlToValidate=&quot;txt_lname&quot;Display=&quot;Dynamic&quot;ForeColor=&quot;Red&quot;&gt;&lt;/asp:RequiredFieldValidator&gt;
&lt;/div&gt;
&lt;/div&gt;
&lt;/div&gt;
&lt;divclass=&quot;form-group&quot;&gt;
&lt;labelfor=&quot;exampleInputEmail1&quot;&gt;Email address&lt;/label&gt;
&lt;asp:TextBoxID=&quot;txt_email&quot;runat=&quot;server&quot;CssClass=&quot;form-control&quot;placeholder=&quot;Enter
email&quot;TextMode=&quot;Email&quot;&gt;&lt;/asp:TextBox&gt;
&lt;asp:RequiredFieldValidatorID=&quot;rqr_emil&quot;runat=&quot;server&quot;ErrorMessage=&quot;Enter
email&quot;ControlToValidate=&quot;txt_email&quot;Display=&quot;Dynamic&quot;ForeColor=&quot;Red&quot;&gt;&lt;/asp:RequiredFieldValidator&gt;
&lt;asp:RegularExpressionValidatorID=&quot;rqrexpre_email&quot;runat=&quot;server&quot;ErrorMessage=&quot;Enter validate
email&quot;ValidationExpression=&quot;\w+([-+.&#39;]\w+)*@\w+([-.]\w+)*\.\w+([-
.]\w+)*&quot;ControlToValidate=&quot;txt_email&quot;Display=&quot;Dynamic&quot;ForeColor=&quot;Red&quot;&gt;&lt;/asp:RegularExpressionValidator&gt;
&lt;/div&gt;
&lt;divclass=&quot;form-group&quot;&gt;
&lt;divclass=&quot;form-row&quot;&gt;
&lt;divclass=&quot;col-md-6&quot;&gt;
&lt;labelfor=&quot;exampleInputPassword1&quot;&gt;Password&lt;/label&gt;
&lt;asp:TextBoxID=&quot;txt_pass&quot;runat=&quot;server&quot;CssClass=&quot;form-control&quot;placeholder=&quot;Enter
password&quot;TextMode=&quot;Password&quot;&gt;&lt;/asp:TextBox&gt;
&lt;asp:RequiredFieldValidatorID=&quot;rqr_pass&quot;runat=&quot;server&quot;ErrorMessage=&quot;Enter
password&quot;ControlToValidate=&quot;txt_pass&quot;Display=&quot;Dynamic&quot;ForeColor=&quot;Red&quot;&gt;&lt;/asp:RequiredFieldValidator&gt;
&lt;/div&gt;
&lt;divclass=&quot;col-md-6&quot;&gt;
&lt;labelfor=&quot;exampleConfirmPassword&quot;&gt;Confirm password&lt;/label&gt;
&lt;asp:TextBoxID=&quot;txt_repass&quot;runat=&quot;server&quot;CssClass=&quot;form-control&quot;placeholder=&quot;Re-type
password&quot;TextMode=&quot;Password&quot;&gt;&lt;/asp:TextBox&gt;
&lt;asp:CompareValidatorID=&quot;rqrcopm_pass&quot;runat=&quot;server&quot;ErrorMessage=&quot;Password do not
match&quot;ControlToValidate=&quot;txt_repass&quot;Display=&quot;Dynamic&quot;ForeColor=&quot;Red&quot;ControlToCompare=&quot;txt_pass&quot;&gt;&lt;/asp:
CompareValidator&gt;
&lt;/div&gt;
&lt;/div&gt;
&lt;/div&gt;
&lt;asp:ButtonID=&quot;btn_register&quot;runat=&quot;server&quot;Text=&quot;Register&quot;CssClass=&quot;btn btn-primary btn-
block&quot;OnClick=&quot;btn_register_Click&quot;/&gt;
&lt;divclass=&quot;text-center&quot;&gt;
&lt;aclass=&quot;d-block small mt-3&quot;href=&quot;login.aspx&quot;&gt;Login Page&lt;/a&gt;
&lt;aclass=&quot;d-block small&quot;href=&quot;forgotpassword.aspx&quot;&gt;Forgot Password?&lt;/a&gt;
&lt;/div&gt;
&lt;/form&gt;
&lt;/div&gt;
&lt;/div&gt;

55 | Page

&lt;/div&gt;
&lt;/body&gt;
&lt;/html&gt;
 Register.aspx.cs
using System;
using System.Collections.Generic;
using System.Linq;
using System.Web;
using System.Web.UI;
using System.Web.UI.WebControls;
using System.Data.SqlClient;
using System.Data;
using System.Configuration;
publicpartialclassregister : System.Web.UI.Page
{
protectedvoid Page_Load(object sender, EventArgs e)
{
if (!IsPostBack)
{
}
}
protectedvoid btn_register_Click(object sender, EventArgs e)
{
if (Page.IsValid)
{
string s = ConfigurationManager.ConnectionStrings[&quot;dbcs&quot;].ConnectionString;
using (SqlConnection con = new SqlConnection(s))
{
SqlCommand cmd = new SqlCommand(&quot;spUsersRegisterinsert&quot;, con);
cmd.CommandType = CommandType.StoredProcedure;
cmd.Parameters.AddWithValue(&quot;@user_fname&quot;, txt_fname.Text);
cmd.Parameters.AddWithValue(&quot;@user_lname&quot;, txt_lname.Text);
cmd.Parameters.AddWithValue(&quot;@email&quot;, txt_email.Text);
cmd.Parameters.AddWithValue(&quot;@password&quot;, txt_pass.Text);
try
{
con.Open();
int value = (int)cmd.ExecuteScalar(); // as procedure return number
if (value == 1)
{
Response.Redirect(&quot;~/Login.aspx?register=successfull&quot;);
}
else
{
pnl_warning.Visible = true;
lbl_warning.Text = &quot;Email is already in use&quot;;
}
}
catch (Exception ex)
{
pnl_warning.Visible = true;
lbl_warning.Text = &quot;Something went wrong! Contact your devloper &lt;/br&gt;&quot; +ex.Message;
}
}

56 | Page

}
else
{
pnl_warning.Visible = true;
lbl_warning.Text = &quot;Please fill all the requirements&quot;;
}
}
}
 Index.aspx
&lt;%@PageTitle=&quot;&quot;Language=&quot;C#&quot;MasterPageFile=&quot;~/usermaster.master&quot;AutoEventWireup=&quot;true&quot;CodeFile=&quot;inde
x.aspx.cs&quot;Inherits=&quot;_Default&quot;%&gt;
&lt;asp:ContentID=&quot;Content1&quot;ContentPlaceHolderID=&quot;heardcontentplaceholder&quot;runat=&quot;Server&quot;&gt;
&lt;/asp:Content&gt;
&lt;asp:ContentID=&quot;Content2&quot;ContentPlaceHolderID=&quot;maincontentplaceholder&quot;runat=&quot;Server&quot;&gt;
&lt;h2class=&quot;my-4&quot;&gt;Category&lt;/h2&gt;
&lt;hr/&gt;
&lt;!-- Category Section --&gt;
&lt;divclass=&quot;row&quot;&gt;
&lt;asp:RepeaterID=&quot;gridview_categorylist&quot;runat=&quot;server&quot;&gt;
&lt;ItemTemplate&gt;
&lt;divclass=&quot;col-lg-3 mb-3&quot;&gt;
&lt;divclass=&quot;card h-100 text-center&quot;&gt;
&lt;h4class=&quot;card-header&quot;&gt;&lt;%# Eval(&quot;category_name&quot;) %&gt;&lt;/h4&gt;
&lt;divclass=&quot;card-footer&quot;&gt;
&lt;asp:HyperLinkID=&quot;btn_category&quot;runat=&quot;server&quot;CssClass=&quot;btn btn-
primary&quot;ForeColor=&quot;White&quot;NavigateUrl=&#39;&lt;%#&quot;~/categoryitem.aspx?cid=&quot; + Eval(&quot;category_id&quot;) %&gt;&#39;&gt;Go to
subjects&lt;/asp:HyperLink&gt;
&lt;/div&gt;
&lt;/div&gt;
&lt;/div&gt;
&lt;/ItemTemplate&gt;
&lt;/asp:Repeater&gt;
&lt;divclass=&quot;col-md-12&quot;&gt;
&lt;divclass=&quot;card&quot;&gt;
&lt;divclass=&quot;card-header&quot;&gt;
&lt;asp:PanelID=&quot;panel_categoryshow_warning&quot;runat=&quot;server&quot;Visible=&quot;false&quot;&gt;
&lt;br/&gt;
&lt;divclass=&quot;alert alert-danger text-center&quot;&gt;
&lt;asp:LabelID=&quot;lbl_categoryshowwarning&quot;runat=&quot;server&quot;/&gt;
&lt;/div&gt;
&lt;/asp:Panel&gt;
&lt;/div&gt;
&lt;/div&gt;
&lt;/div&gt;
&lt;/div&gt;
&lt;/asp:Content&gt;
 Index.aspx.cs
using System;
using System.Collections.Generic;
using System.Linq;
using System.Web;
using System.Web.UI;
using System.Web.UI.WebControls;
using System.Data.SqlClient;

57 | Page

using System.Data;
using System.Configuration;
publicpartialclass_Default : System.Web.UI.Page
{
protectedvoid Page_Load(object sender, EventArgs e)
{
categorylistmethod();
}
string s = ConfigurationManager.ConnectionStrings[&quot;dbcs&quot;].ConnectionString;
//method for categorylist
publicvoid categorylistmethod()
{
using (SqlConnection con = new SqlConnection(s))
{
SqlCommand cmd = new SqlCommand(&quot;select * from category&quot;, con);
try
{
con.Open();
SqlDataReader rd = cmd.ExecuteReader();
if (rd.HasRows)
{
gridview_categorylist.DataSource = rd;
gridview_categorylist.DataBind();
}
else
{
panel_categoryshow_warning.Visible = true;
lbl_categoryshowwarning.Text = &quot;Sorry! There is no category&quot;;
}
}
catch (Exception ex)
{
panel_categoryshow_warning.Visible = true;
lbl_categoryshowwarning.Text = &quot;Something went wrong. Please try after sometime later&lt;/br&gt; Contact
you developer for this problem &quot; + ex.Message;
}
}
}
}
 Question.aspx
&lt;%@PageTitle=&quot;&quot;Language=&quot;C#&quot;MasterPageFile=&quot;~/usermaster.master&quot;AutoEventWireup=&quot;true&quot;CodeFile=&quot;quest
ion.aspx.cs&quot;Inherits=&quot;exam&quot;%&gt;
&lt;asp:ContentID=&quot;Content1&quot;ContentPlaceHolderID=&quot;heardcontentplaceholder&quot;runat=&quot;Server&quot;&gt;
&lt;/asp:Content&gt;
&lt;asp:ContentID=&quot;Content2&quot;ContentPlaceHolderID=&quot;maincontentplaceholder&quot;runat=&quot;Server&quot;&gt;
&lt;h2class=&quot;m-4&quot;&gt;Answer all the questions&lt;/h2&gt;
&lt;hr/&gt;
&lt;asp:TextBoxID=&quot;getstringuser&quot;runat=&quot;server&quot;Visible=&quot;false&quot;&gt;&lt;/asp:TextBox&gt;
&lt;asp:GridViewID=&quot;gridview_examquestion&quot;runat=&quot;server&quot;AutoGenerateColumns=&quot;False&quot;GridLines=&quot;None&quot;&gt;
&lt;Columns&gt;
&lt;asp:TemplateField&gt;
&lt;ItemTemplate&gt;

58 | Page

&lt;asp:LabelID=&quot;lblid&quot;runat=&quot;server&quot;Text=&#39;&lt;%# Eval(&quot;question_id&quot;) %&gt;&#39;Visible=&quot;false&quot;&gt;&lt;/asp:Label&gt;
&lt;asp:LabelID=&quot;lbl_question&quot;runat=&quot;server&quot;Text=&#39;&lt;%# Eval(&quot;question_name&quot;) %&gt;&#39;&gt;&lt;/asp:Label&gt;
&lt;br/&gt;
&lt;asp:RadioButtonGroupName=&quot;a&quot;Text=&#39;&lt;%# Eval(&quot;option_one&quot;) %&gt;&#39;ID=&quot;option_one&quot;runat=&quot;server&quot;/&gt;
&lt;br/&gt;
&lt;asp:RadioButtonGroupName=&quot;a&quot;Text=&#39;&lt;%# Eval(&quot;option_two&quot;) %&gt;&#39;ID=&quot;option_two&quot;runat=&quot;server&quot;/&gt;
&lt;br/&gt;
&lt;asp:RadioButtonGroupName=&quot;a&quot;Text=&#39;&lt;%# Eval(&quot;option_three&quot;) %&gt;&#39;ID=&quot;option_three&quot;runat=&quot;server&quot;/&gt;
&lt;br/&gt;
&lt;asp:RadioButtonGroupName=&quot;a&quot;Text=&#39;&lt;%# Eval(&quot;option_four&quot;) %&gt;&#39;ID=&quot;option_four&quot;runat=&quot;server&quot;/&gt;
&lt;hr/&gt;
&lt;/ItemTemplate&gt;
&lt;/asp:TemplateField&gt;
&lt;/Columns&gt;
&lt;/asp:GridView&gt;
&lt;asp:ButtonID=&quot;btn_submit&quot;runat=&quot;server&quot;Text=&quot;Submit&quot;CssClass=&quot;btn btn-
success&quot;OnClick=&quot;btn_submit_Click&quot;/&gt;
&lt;divclass=&quot;col-md-12&quot;&gt;
&lt;divclass=&quot;card&quot;&gt;
&lt;divclass=&quot;card-header&quot;&gt;
&lt;asp:PanelID=&quot;panel_questshow_warning&quot;runat=&quot;server&quot;Visible=&quot;false&quot;&gt;
&lt;br/&gt;
&lt;divclass=&quot;alert alert-danger text-center&quot;&gt;
&lt;asp:LabelID=&quot;lbl_questshowwarning&quot;runat=&quot;server&quot;/&gt;
&lt;/div&gt;
&lt;/asp:Panel&gt;
&lt;/div&gt;
&lt;/div&gt;
&lt;/div&gt;
&lt;/asp:Content&gt;
 Question.aspx.cs
using System;
using System.Collections.Generic;
using System.Linq;
using System.Web;
using System.Web.UI;
using System.Web.UI.WebControls;
using System.Data.SqlClient;
using System.Data;
using System.Configuration;

publicpartialclassexam : System.Web.UI.Page

{
protectedvoid Page_Load(object sender, EventArgs e)
{
HttpCookie usercookie = Request.Cookies[&quot;user_cookies&quot;];
if (Session[&quot;Useremail&quot;] != null || usercookie != null)
{
if (Session[&quot;Useremail&quot;] == null)
{
getstringuser.Text = usercookie[&quot;Useremail&quot;];
}
else
{
getstringuser.Text = Session[&quot;Useremail&quot;].ToString();
}

59 | Page

}
else
{
Response.Redirect(&quot;~/login.aspx&quot;);
}
if (!IsPostBack)
{
string eid = Request.QueryString[&quot;eid&quot;];
if (eid == null)
{
Response.Redirect(&quot;index.aspx&quot;);
}
questionistmethod(Convert.ToInt32(eid));
}
}
string s = ConfigurationManager.ConnectionStrings[&quot;dbcs&quot;].ConnectionString;
//method for getting question
publicvoid questionistmethod(int id)
{
using (SqlConnection con = new SqlConnection(s))
{
SqlCommand cmd = new SqlCommand(&quot;spQuestionserachexam&quot;, con);
cmd.CommandType = CommandType.StoredProcedure;
cmd.Parameters.AddWithValue(&quot;@examid&quot;, id);
try
{
con.Open();
SqlDataReader rd = cmd.ExecuteReader();
if (rd.HasRows)
{
gridview_examquestion.DataSource = rd;
gridview_examquestion.DataBind();
}
else
{
panel_questshow_warning.Visible = true;
lbl_questshowwarning.Text = &quot;Sorry! There is no question in this exam&quot;;
}
}
catch (Exception ex)
{
panel_questshow_warning.Visible = true;
lbl_questshowwarning.Text = &quot;Something went wrong. Please try after sometime later&lt;/br&gt; Contact you
developer for this problem&quot; + ex.Message;
}
}
}
//decalring some varibles to exam marking
string result = string.Empty;
string examname;
int select_number = 0;
int correct_number = 0;
int wrong_number = 0;
int count = 0;
protectedvoid btn_submit_Click(object sender, EventArgs e)

60 | Page

{
foreach (GridViewRow row in gridview_examquestion.Rows)
{
Label li = row.FindControl(&quot;lblid&quot;) as Label;
RadioButton r1 = row.FindControl(&quot;option_one&quot;) as RadioButton;
RadioButton r2 = row.FindControl(&quot;option_two&quot;) as RadioButton;
RadioButton r3 = row.FindControl(&quot;option_three&quot;) as RadioButton;
RadioButton r4 = row.FindControl(&quot;option_four&quot;) as RadioButton;
if (r1.Checked == true)
{
select_number = 1;
}
elseif (r2.Checked == true)
{
select_number = 2;
}
elseif (r3.Checked == true)
{
select_number = 3;
}
elseif (r4.Checked == true)
{
select_number = 4;
}
checkanwer(li.Text);
panel_questshow_warning.Visible = false;
}
saveinresult(passfail(), correct_number, gridview_examquestion.Rows.Count);
}//method for checking answer wheter it is right or wrong
publicvoid checkanwer(string qid)
{
using (SqlConnection con = new SqlConnection(s))
{
SqlCommand cmd = new SqlCommand();
cmd.CommandText = &quot;select * from question where question_id = @questionid&quot; + count;
cmd.Parameters.AddWithValue(&quot;@questionid&quot; + count, qid);
cmd.Connection = con;
try
{
con.Open();
SqlDataReader rd = cmd.ExecuteReader();
while (rd.Read())
{
if (select_number == Convert.ToInt32(rd[&quot;question_answer&quot;]))
{
correct_number = correct_number + 1;
break;
}
else
{
wrong_number = wrong_number + 1;
break;
}

61 | Page

}
count++;
}
catch (Exception ex)
{
panel_questshow_warning.Visible = true;
lbl_questshowwarning.Text = &quot;Something went wrong. Please try after sometime later&lt;/br&gt; Contact you
developer for this problem&quot; + ex.Message;
}
}
}
//method for cheking if examinee pass or fail from the exam pass mark in database
publicstring passfail()
{
string eid = Request.QueryString[&quot;eid&quot;];
using (SqlConnection con = new SqlConnection(s))
{
SqlCommand cmd = new SqlCommand(&quot;Select exampass_marks from exam where exam_id = @examid&quot;,
con);
cmd.Parameters.AddWithValue(&quot;@examid&quot;, eid);
con.Open();
SqlDataReader rd = cmd.ExecuteReader();
while (rd.Read())
{
if (correct_number &gt;= Convert.ToInt32(rd[&quot;exampass_marks&quot;]))
{
result = result + &quot;Pass&quot;;
break;
}
else
{
result = result + &quot;Fail&quot;;
break;
}
}
}
return result;
}
// method for saving the result info in databse
publicvoid saveinresult(string status, int score, int tquestion)
{
string eid = Request.QueryString[&quot;eid&quot;];
using (SqlConnection con = new SqlConnection(s))
{
SqlCommand cmd = new SqlCommand(&quot;spResultinsert&quot;, con);
cmd.CommandType = CommandType.StoredProcedure;
cmd.Parameters.AddWithValue(&quot;@examfid&quot;, eid);
cmd.Parameters.AddWithValue(&quot;@resultstatus&quot;, status);
cmd.Parameters.AddWithValue(&quot;@resultscore&quot;, score);
cmd.Parameters.AddWithValue(&quot;@totalquestion&quot;, tquestion);
cmd.Parameters.AddWithValue(&quot;@username&quot;, getstringuser.Text);
cmd.Parameters.AddWithValue(&quot;@examdate&quot;, DateTime.Now.ToString());
try
{
con.Open();

62 | Page

cmd.ExecuteNonQuery();
Response.Redirect(&quot;~/index.aspx&quot;);
}
catch (Exception ex)
{
panel_questshow_warning.Visible = true;
lbl_questshowwarning.Text = &quot;Something went wrong. Please try after sometime later&lt;/br&gt; Contact you
developer for this problem&quot; + ex.Message;
}
}
}
}
 Myresult.aspx
&lt;%@PageTitle=&quot;&quot;Language=&quot;C#&quot;MasterPageFile=&quot;~/usermaster.master&quot;AutoEventWireup=&quot;true&quot;CodeFile=&quot;myre
sult.aspx.cs&quot;Inherits=&quot;myresult&quot;%&gt;
&lt;asp:ContentID=&quot;Content1&quot;ContentPlaceHolderID=&quot;heardcontentplaceholder&quot;Runat=&quot;Server&quot;&gt;
&lt;/asp:Content&gt;
&lt;asp:ContentID=&quot;Content2&quot;ContentPlaceHolderID=&quot;maincontentplaceholder&quot;Runat=&quot;Server&quot;&gt;
&lt;divclass=&quot;card-header&quot;&gt;
&lt;h2&gt;My Result&lt;/h2&gt;
&lt;/div&gt;
&lt;asp:TextBoxID=&quot;getemail&quot;runat=&quot;server&quot;Visible=&quot;false&quot;&gt;&lt;/asp:TextBox&gt;
&lt;asp:GridViewID=&quot;gridmyresult&quot;runat=&quot;server&quot;GridLines=&quot;None&quot;AllowPaging=&quot;True&quot;AutoGenerateColumns=&quot;F
alse&quot;CssClass=&quot;table table-bordered&quot;OnPageIndexChanging=&quot;gridmyresult_PageIndexChanging&quot;PageSize=&quot;8&quot;&gt;
&lt;Columns&gt;
&lt;asp:BoundFieldDataField=&quot;exam_name&quot;HeaderText=&quot;Exam Name&quot;NullDisplayText=&quot;no exam name&quot;/&gt;
&lt;asp:BoundFieldDataField=&quot;exam_date&quot;DataFormatString=&quot;{0:M/d/yy}&quot;HeaderText=&quot;Exam
Date&quot;NullDisplayText=&quot;There is some problem to find exam date&quot;/&gt;
&lt;asp:BoundFieldDataField=&quot;totalquestion&quot;HeaderText=&quot;Total Question&quot;/&gt;
&lt;asp:BoundFieldDataField=&quot;result_status&quot;HeaderText=&quot;Result&quot;/&gt;
&lt;asp:BoundFieldDataField=&quot;exam_marks&quot;HeaderText=&quot;Total Marks&quot;/&gt;
&lt;asp:BoundFieldDataField=&quot;result_score&quot;HeaderText=&quot;Your Score&quot;/&gt;
&lt;/Columns&gt;
&lt;/asp:GridView&gt;
&lt;divclass=&quot;col-md-12&quot;&gt;
&lt;divclass=&quot;card&quot;&gt;
&lt;divclass=&quot;card-header&quot;&gt;
&lt;asp:PanelID=&quot;panel_myresultshow_warning&quot;runat=&quot;server&quot;Visible=&quot;false&quot;&gt;
&lt;br/&gt;
&lt;divclass=&quot;alert alert-danger text-center&quot;&gt;
&lt;asp:LabelID=&quot;lbl_myresultshowwarning&quot;runat=&quot;server&quot;/&gt;
&lt;/div&gt;
&lt;/asp:Panel&gt;
&lt;/div&gt;
&lt;/div&gt;
&lt;/div&gt;&lt;/asp:Content&gt;
 Myresult.aspx.cs
using System;
using System.Collections.Generic;
using System.Linq;
using System.Web;
using System.Web.UI;
using System.Web.UI.WebControls;
using System.Data.SqlClient;

63 | Page

using System.Data;
using System.Configuration;
publicpartialclassmyresult : System.Web.UI.Page
{
protectedvoid Page_Load(object sender, EventArgs e)
{
HttpCookie usercookie = Request.Cookies[&quot;user_cookies&quot;];
if (Session[&quot;Useremail&quot;] != null || usercookie != null)
{
if (Session[&quot;Useremail&quot;] == null)
{
getemail.Text = usercookie[&quot;Useremail&quot;];
}
else
{
getemail.Text = Session[&quot;Useremail&quot;].ToString();
}
}
else
{
Response.Redirect(&quot;~/login.aspx&quot;);
}
if (!IsPostBack)
{
getmyresults(getemail.Text);
}
}
string s = ConfigurationManager.ConnectionStrings[&quot;dbcs&quot;].ConnectionString;
publicvoid getmyresults(string email)
{
using (SqlConnection con = new SqlConnection(s))
{
SqlCommand cmd = new SqlCommand(&quot;spUserresult&quot;, con);
cmd.CommandType = CommandType.StoredProcedure;
cmd.Parameters.AddWithValue(&quot;@email&quot;, email);
try
{
con.Open();
using(SqlDataAdapter ad = new SqlDataAdapter())
{
ad.SelectCommand = cmd;
using (DataTable tb = new DataTable())
{
ad.Fill(tb);
if (tb != null)
{
gridmyresult.DataSource = tb;
gridmyresult.DataBind();
}
else
{
panel_myresultshow_warning.Visible = true;
lbl_myresultshowwarning.Text = &quot;Sorry! There is no result of your in this application&quot;;
}
}
}

64 | Page

}
catch (Exception ex)
{
panel_myresultshow_warning.Visible = true;
lbl_myresultshowwarning.Text = &quot;Something went wrong. Please try after sometime later&lt;/br&gt; Contact
you developer for this problem&quot; + ex.Message;
}
}
}
protectedvoid gridmyresult_PageIndexChanging(object sender, GridViewPageEventArgs e)
{
gridmyresult.PageIndex = e.NewPageIndex;
getmyresults(getemail.Text);
}
}
 Adminlogin.aspx
&lt;%@PageLanguage=&quot;C#&quot;AutoEventWireup=&quot;true&quot;CodeFile=&quot;login.aspx.cs&quot;Inherits=&quot;admin_login&quot;%&gt;
&lt;!DOCTYPEhtml&gt;
&lt;htmllang=&quot;en&quot;&gt;
&lt;head&gt;
&lt;metacharset=&quot;utf-8&quot;&gt;
&lt;metahttp-equiv=&quot;X-UA-Compatible&quot;content=&quot;IE=edge&quot;&gt;
&lt;metaname=&quot;viewport&quot;content=&quot;width=device-width, initial-scale=1, shrink-to-fit=no&quot;&gt;
&lt;metaname=&quot;description&quot;content=&quot;&quot;&gt;
&lt;metaname=&quot;author&quot;content=&quot;&quot;&gt;
&lt;title&gt;Login - Online exam sytem&lt;/title&gt;
&lt;!-- Bootstrap core CSS--&gt;
&lt;linkhref=&quot;../assets/css/bootstrap.min.css&quot;rel=&quot;stylesheet&quot;&gt;
&lt;!-- Custom fonts for login--&gt;
&lt;linkhref=&quot;../assets/css/custom.css&quot;rel=&quot;stylesheet&quot;&gt;
&lt;/head&gt;
&lt;bodyclass=&quot;bg-dark&quot;&gt;
&lt;divclass=&quot;container&quot;&gt;
&lt;divclass=&quot;card card-login mx-auto mt-5&quot;&gt;
&lt;divclass=&quot;card-header&quot;&gt;Admin Login&lt;/div&gt;
&lt;divclass=&quot;card-body&quot;&gt;
&lt;formrunat=&quot;server&quot;id=&quot;formlogin&quot;&gt;
&lt;asp:PanelID=&quot;pnl_warning&quot;runat=&quot;server&quot;Visible=&quot;false&quot;&gt;
&lt;divclass=&quot;form-group card-header text-center&quot;&gt;
&lt;divclass=&quot;alert-danger&quot;&gt;
&lt;asp:LabelID=&quot;lbl_warning&quot;runat=&quot;server&quot;Text=&quot;Label&quot;CssClass=&quot;col-form-label text-center&quot;&gt;&lt;/asp:Label&gt;
&lt;/div&gt;
&lt;/div&gt;
&lt;/asp:Panel&gt;
&lt;divclass=&quot;form-group&quot;&gt;
&lt;labelfor=&quot;exampleInputEmail1&quot;&gt;Email address&lt;/label&gt;
&lt;asp:TextBoxID=&quot;txt_email&quot;runat=&quot;server&quot;CssClass=&quot;form-control&quot;placeholder=&quot;Enter
email&quot;TextMode=&quot;Email&quot;&gt;&lt;/asp:TextBox&gt;
&lt;asp:RequiredFieldValidatorID=&quot;rqr_emil&quot;runat=&quot;server&quot;ErrorMessage=&quot;Enter
email&quot;ControlToValidate=&quot;txt_email&quot;Display=&quot;Dynamic&quot;ForeColor=&quot;Red&quot;&gt;&lt;/asp:RequiredFieldValidator&gt;
&lt;asp:RegularExpressionValidatorID=&quot;rqrexpre_email&quot;runat=&quot;server&quot;ErrorMessage=&quot;Enter validate
email&quot;ValidationExpression=&quot;\w+([-+.&#39;]\w+)*@\w+([-.]\w+)*\.\w+([-
.]\w+)*&quot;ControlToValidate=&quot;txt_email&quot;Display=&quot;Dynamic&quot;ForeColor=&quot;Red&quot;&gt;&lt;/asp:RegularExpressionValidator&gt;

65 | Page

&lt;/div&gt;
&lt;divclass=&quot;form-group&quot;&gt;
&lt;divclass=&quot;form-row&quot;&gt;
&lt;divclass=&quot;col-md-6&quot;&gt;
&lt;labelfor=&quot;exampleInputPassword1&quot;&gt;Password&lt;/label&gt;
&lt;asp:TextBoxID=&quot;txt_pass&quot;runat=&quot;server&quot;CssClass=&quot;form-control&quot;placeholder=&quot;Enter
password&quot;TextMode=&quot;Password&quot;&gt;&lt;/asp:TextBox&gt;
&lt;asp:RequiredFieldValidatorID=&quot;rqr_pass&quot;runat=&quot;server&quot;ErrorMessage=&quot;Enter
password&quot;ControlToValidate=&quot;txt_pass&quot;Display=&quot;Dynamic&quot;ForeColor=&quot;Red&quot;&gt;&lt;/asp:RequiredFieldValidator&gt;
&lt;/div&gt;
&lt;divclass=&quot;col-md-6&quot;&gt;
&lt;labelfor=&quot;exampleConfirmPassword&quot;&gt;Confirm password&lt;/label&gt;
&lt;asp:TextBoxID=&quot;txt_repass&quot;runat=&quot;server&quot;CssClass=&quot;form-control&quot;placeholder=&quot;Re-type
password&quot;TextMode=&quot;Password&quot;&gt;&lt;/asp:TextBox&gt;
&lt;asp:CompareValidatorID=&quot;rqrcopm_pass&quot;runat=&quot;server&quot;ErrorMessage=&quot;Password do not
match&quot;ControlToValidate=&quot;txt_repass&quot;Display=&quot;Dynamic&quot;ForeColor=&quot;Red&quot;ControlToCompare=&quot;txt_pass&quot;&gt;&lt;/asp:
CompareValidator&gt;
&lt;/div&gt;
&lt;/div&gt;
&lt;/div&gt;
&lt;divclass=&quot;form-group&quot;&gt;
&lt;divclass=&quot;form-check&quot;&gt;
&lt;labelclass=&quot;form-check-label&quot;&gt;
&lt;asp:CheckBoxID=&quot;chk_remember&quot;runat=&quot;server&quot;CssClass=&quot;form-check-input remembermecustom&quot;/&gt;
Remember Password&lt;/label&gt;
&lt;/div&gt;
&lt;/div&gt;
&lt;asp:ButtonID=&quot;btn_login&quot;runat=&quot;server&quot;Text=&quot;Log In&quot;CssClass=&quot;btn btn-primary btn-
block&quot;OnClick=&quot;btn_login_Click&quot;/&gt;
&lt;divclass=&quot;text-center&quot;&gt;
&lt;aclass=&quot;d-block small&quot;href=&quot;../HomePage.aspx&quot;&gt;Go To Home Page&lt;/a&gt;
&lt;/div&gt;
&lt;/form&gt;
&lt;/div&gt;
&lt;/div&gt;
&lt;/div&gt;
&lt;/body&gt;
&lt;/html&gt;
 Adminlogin.aspx.cs
using System;
using System.Collections.Generic;
using System.Linq;
using System.Web;
using System.Web.UI;
using System.Web.UI.WebControls;
using System.Data.SqlClient;
using System.Data;
using System.Configuration;
publicpartialclassadmin_login : System.Web.UI.Page
{
protectedvoid Page_Load(object sender, EventArgs e)
{
}
string s = ConfigurationManager.ConnectionStrings[&quot;dbcs&quot;].ConnectionString;

66 | Page

//for login
protectedvoid btn_login_Click(object sender, EventArgs e)
{
if (Page.IsValid)
{
using (SqlConnection con = new SqlConnection(s))
{
SqlCommand cmd = new SqlCommand(&quot;spAdminlogin&quot;, con);
cmd.CommandType = CommandType.StoredProcedure;
cmd.Parameters.AddWithValue(&quot;@admin_email&quot;, txt_email.Text);
cmd.Parameters.AddWithValue(&quot;@password&quot;, txt_pass.Text);
try
{
con.Open();
int value = (int)cmd.ExecuteScalar();
if (value == 1)
{
if (chk_remember.Checked)
{
HttpCookie user = new HttpCookie(&quot;admin_cookies&quot;); //creating cookie object where
user_cookies is cookie name
user[&quot;adminemail&quot;] = txt_email.Text; // cookie content
user.Expires = DateTime.Now.AddYears(3); // give the time/duration of cookie
Response.Cookies.Add(user); // it gives the response in browser
}
else
{
Session[&quot;adminemail&quot;] = txt_email.Text;
}
Response.Redirect(&quot;~/admin/Index.aspx&quot;);
}
else
{
pnl_warning.Visible = true;
lbl_warning.Text = &quot;Use correct email and password&lt;/br&gt;&quot;;
}
}
catch (Exception ex)
{
pnl_warning.Visible = true;
lbl_warning.Text = &quot;Something went wrong! Contact your devloper &lt;/br&gt;&quot; + ex.Message;
}
}
}
else
{
pnl_warning.Visible = true;
lbl_warning.Text = &quot;Please fill all the requirements&quot;;
}
}
}
 Adminstudentlist.aspx
&lt;%@PageTitle=&quot;&quot;Language=&quot;C#&quot;MasterPageFile=&quot;~/admin.master&quot;AutoEventWireup=&quot;true&quot;CodeFile=&quot;studentLi
st.aspx.cs&quot;Inherits=&quot;admin_studentList&quot;%&gt;

67 | Page

&lt;asp:ContentID=&quot;Content1&quot;ContentPlaceHolderID=&quot;headplaceholder&quot;runat=&quot;Server&quot;&gt;
&lt;/asp:Content&gt;
&lt;asp:ContentID=&quot;Content2&quot;ContentPlaceHolderID=&quot;maincontent&quot;runat=&quot;Server&quot;&gt;
&lt;divclass=&quot;col-md-12&quot;&gt;
&lt;divclass=&quot;card&quot;&gt;
&lt;%--Button For select panel--%&gt;
&lt;divclass=&quot;btn-group bg-danger&quot;&gt;
&lt;asp:ButtonID=&quot;btn_panelresult&quot;runat=&quot;server&quot;Text=&quot;All students&quot;CssClass=&quot;btn btn-
info&quot;BorderStyle=&quot;None&quot;CausesValidation=&quot;False&quot;BackColor=&quot;#343A40&quot;/&gt;
&lt;/div&gt;
&lt;divclass=&quot;card text-center mb-3&quot;&gt;
&lt;divclass=&quot;card-body&quot;&gt;
&lt;divclass=&quot;table-responsive&quot;&gt;
&lt;asp:GridViewID=&quot;gridallstudents&quot;runat=&quot;server&quot;GridLines=&quot;None&quot;AllowPaging=&quot;True&quot;AutoGenerateColumns=&quot;
False&quot;CssClass=&quot;table table-
bordered&quot;PageSize=&quot;8&quot;OnPageIndexChanging=&quot;gridallstudents_PageIndexChanging&quot;&gt;
&lt;Columns&gt;
&lt;asp:BoundFieldDataField=&quot;user_fname&quot;HeaderText=&quot;First name&quot;/&gt;
&lt;asp:BoundFieldDataField=&quot;user_lname&quot;HeaderText=&quot;Last name&quot;/&gt;
&lt;asp:BoundFieldDataField=&quot;user_email&quot;HeaderText=&quot;Email&quot;/&gt;
&lt;asp:TemplateFieldHeaderText=&quot;Result&quot;&gt;
&lt;ItemTemplate&gt;
&lt;asp:HyperLinkID=&quot;btn_viewquestion&quot;runat=&quot;server&quot;CssClass=&quot;btn&quot;BackColor=&quot;#343A40&quot;BorderStyle=&quot;None&quot;F
oreColor=&quot;White&quot;NavigateUrl=&#39;&lt;%#&quot;~/admin/result.aspx?uid=&quot; + Eval(&quot;user_email&quot;) %&gt;&#39;&gt;
&lt;iclass=&quot;fa fa-info-circle&quot;aria-hidden=&quot;true&quot;&gt;&lt;/i&gt; View Result
&lt;/asp:HyperLink&gt;
&lt;/ItemTemplate&gt;
&lt;/asp:TemplateField&gt;
&lt;/Columns&gt;
&lt;/asp:GridView&gt;
&lt;/div&gt;
&lt;/div&gt;
&lt;asp:PanelID=&quot;panel_studentlistshow_warning&quot;runat=&quot;server&quot;Visible=&quot;false&quot;&gt;
&lt;divclass=&quot;card-footer&quot;&gt;
&lt;br/&gt;
&lt;divclass=&quot;alert alert-danger text-center&quot;&gt;
&lt;asp:LabelID=&quot;lbl_studentlistshowwarning&quot;runat=&quot;server&quot;/&gt;
&lt;/div&gt;
&lt;/div&gt;
&lt;/asp:Panel&gt;
&lt;/div&gt;
&lt;/div&gt;
&lt;/div&gt;
&lt;/asp:Content&gt;
 Adminstudentlist.aspx.cs
using System;
using System.Collections.Generic;
using System.Linq;
using System.Web;
using System.Web.UI;
using System.Web.UI.WebControls;
using System.Data.SqlClient;
using System.Data;
using System.Configuration;

68 | Page

publicpartialclassadmin_studentList : System.Web.UI.Page
{
protectedvoid Page_Load(object sender, EventArgs e)
{
if (!IsPostBack)
{
getallstudents();
}
}
string s = ConfigurationManager.ConnectionStrings[&quot;dbcs&quot;].ConnectionString;
//method for get all result
publicvoid getallstudents()
{
using (SqlConnection con = new SqlConnection(s))
{
SqlCommand cmd = new SqlCommand(&quot;select * from users&quot;, con);
try
{
con.Open();
using (SqlDataAdapter ad = new SqlDataAdapter())
{
ad.SelectCommand = cmd;
using (DataTable tb = new DataTable())
{
ad.Fill(tb);
if (tb != null)
{
gridallstudents.DataSource = tb;
gridallstudents.DataBind();
}
else
{
panel_studentlistshow_warning.Visible = true;
lbl_studentlistshowwarning.Text = &quot;There is no result right now in this application&quot;;
}
}
}
}
catch (Exception ex)
{
panel_studentlistshow_warning.Visible = true;
lbl_studentlistshowwarning.Text = &quot;Something went wrong. Please try after sometime later&lt;/br&gt; Contact
you developer for this problem&quot; + ex.Message;
}
}
}
//for paging
protectedvoid gridallstudents_PageIndexChanging(object sender, GridViewPageEventArgs e)
{
gridallstudents.PageIndex = e.NewPageIndex;
getallstudents();
}
}

69 | Page

 Editcategory.aspx
&lt;%@PageTitle=&quot;&quot;Language=&quot;C#&quot;MasterPageFile=&quot;~/admin.master&quot;AutoEventWireup=&quot;true&quot;CodeFile=&quot;editcateg
ory.aspx.cs&quot;Inherits=&quot;admin_editcategory&quot;%&gt;
&lt;asp:ContentID=&quot;Content1&quot;ContentPlaceHolderID=&quot;headplaceholder&quot;Runat=&quot;Server&quot;&gt;
&lt;/asp:Content&gt;
&lt;asp:ContentID=&quot;Content2&quot;ContentPlaceHolderID=&quot;maincontent&quot;Runat=&quot;Server&quot;&gt;
&lt;divclass=&quot;col-md-12&quot;&gt;
&lt;divclass=&quot;card&quot;&gt;
&lt;%--Button For select panel--%&gt;
&lt;divclass=&quot;btn-group bg-danger&quot;&gt;
&lt;asp:ButtonID=&quot;btn_panelcategorylist&quot;runat=&quot;server&quot;Text=&quot;Edit Category&quot;CssClass=&quot;btn btn-
info&quot;BorderStyle=&quot;None&quot;CausesValidation=&quot;False&quot;BackColor=&quot;#343A40&quot;/&gt;
&lt;/div&gt;
&lt;%--Add category --%&gt;
&lt;divclass=&quot;card-body&quot;&gt;
&lt;divclass=&quot;row form-group&quot;&gt;
&lt;labelclass=&quot;col-md-2 col-form-label &quot;&gt;Category Name&lt;/label&gt;
&lt;divclass=&quot;col-md-4&quot;&gt;
&lt;asp:TextBoxID=&quot;txt_categoryedit&quot;runat=&quot;server&quot;CssClass=&quot;form-control&quot;&gt;&lt;/asp:TextBox&gt;
&lt;asp:RequiredFieldValidatorID=&quot;require_category&quot;runat=&quot;server&quot;ErrorMessage=&quot;Enter
category&quot;ControlToValidate=&quot;txt_categoryedit&quot;ForeColor=&quot;red&quot;&gt;&lt;/asp:RequiredFieldValidator&gt;
&lt;/div&gt;
&lt;/div&gt;
&lt;divclass=&quot;card-footer&quot;&gt;
&lt;divclass=&quot;offset-2&quot;&gt;
&lt;asp:ButtonID=&quot;btn_editcategory&quot;runat=&quot;server&quot;Text=&quot;Edit
Category&quot;CssClass=&quot;btn&quot;BackColor=&quot;#343A40&quot;BorderStyle=&quot;None&quot;ForeColor=&quot;White&quot;OnClick=&quot;btn_editcategor
y_Click&quot;/&gt;
&lt;/div&gt;
&lt;asp:PanelID=&quot;panel_editcategory_warning&quot;runat=&quot;server&quot;Visible=&quot;false&quot;&gt;
&lt;br/&gt;
&lt;divclass=&quot;alert alert-danger text-center&quot;&gt;
&lt;asp:LabelID=&quot;lbl_categoryeditwarning&quot;runat=&quot;server&quot;/&gt;
&lt;/div&gt;
&lt;/asp:Panel&gt;
&lt;/div&gt;
&lt;/div&gt;
&lt;/div&gt;
&lt;/div&gt;
&lt;/asp:Content&gt;
 Editcategory.aspx.cs
using System;
using System.Collections.Generic;
using System.Linq;
using System.Web;
using System.Web.UI;
using System.Web.UI.WebControls;
using System.Data.SqlClient;
using System.Configuration;
using System.Data;
publicpartialclassadmin_editcategory : System.Web.UI.Page
{
protectedvoid Page_Load(object sender, EventArgs e)

70 | Page

{
if (!IsPostBack)
{
string category_id = Request.QueryString[&quot;cid&quot;];
if(category_id == null)
{
Response.Redirect(&quot;~/admin/category.aspx&quot;);
}
txt_categoryedit.Focus();
categoryedit_fill(Convert.ToInt32(category_id)); //calling method with parametres
}
}
//for update the category
protectedvoid btn_editcategory_Click(object sender, EventArgs e)
{
string category_id = Request.QueryString[&quot;cid&quot;];
if (IsValid)
{
string cs = ConfigurationManager.ConnectionStrings[&quot;dbcs&quot;].ConnectionString;
using (SqlConnection con = new SqlConnection(cs))
{
SqlCommand cmd = new SqlCommand(&quot;update category set category_name= @category_name where
category_id = @categoryid&quot;, con);
cmd.Parameters.AddWithValue(&quot;@categoryid&quot;, Convert.ToInt32(category_id));
cmd.Parameters.AddWithValue(&quot;@category_name&quot;, txt_categoryedit.Text);
try
{
con.Open();
int i = (int)cmd.ExecuteNonQuery();
if (i &gt; 0)
{
Response.Redirect(&quot;~/admin/category.aspx&quot;);
}
else
{
txt_categoryedit.Focus();
panel_editcategory_warning.Visible = true;
lbl_categoryeditwarning.Text = &quot;Something went wrong. Can&#39;t update. Please try after sometime
later&lt;/br&gt; &quot;;
}
}
catch (Exception ex)
{
txt_categoryedit.Focus();
panel_editcategory_warning.Visible = true;
lbl_categoryeditwarning.Text = &quot;Something went wrong. Please try after sometime later&lt;/br&gt; Contact
you developer for this problem&quot; + ex.Message;
}
} // end of using
}
else
{
txt_categoryedit.Focus();
panel_editcategory_warning.Visible = true;
lbl_categoryeditwarning.Text = &quot;You must fill all the requirements&quot;;
}

71 | Page

}
//edit fill method
publicvoid categoryedit_fill(int id)
{
string cs = ConfigurationManager.ConnectionStrings[&quot;dbcs&quot;].ConnectionString;
using (SqlConnection con = new SqlConnection(cs))
{
SqlCommand cmd = new SqlCommand(&quot;select * from category where category_id = @cid&quot;, con);
cmd.Parameters.AddWithValue(&quot;@cid&quot;, id);
try
{
con.Open();
SqlDataReader rd = cmd.ExecuteReader();
while (rd.Read())
{
txt_categoryedit.Text = rd[&quot;category_name&quot;].ToString();
}
}
catch (Exception ex)
{
panel_editcategory_warning.Visible = true;
lbl_categoryeditwarning.Text = &quot;Something went wrong. Please try after sometime later&lt;/br&gt; Contact you
developer for this problem&quot; + ex.Message;
}
}
}
}
 Editsubject.aspx
&lt;%@PageTitle=&quot;&quot;Language=&quot;C#&quot;MasterPageFile=&quot;~/admin.master&quot;AutoEventWireup=&quot;true&quot;CodeFile=&quot;editsubje
ct.aspx.cs&quot;Inherits=&quot;admin_editsubject&quot;%&gt;
&lt;asp:ContentID=&quot;Content1&quot;ContentPlaceHolderID=&quot;headplaceholder&quot;Runat=&quot;Server&quot;&gt;
&lt;/asp:Content&gt;
&lt;asp:ContentID=&quot;Content2&quot;ContentPlaceHolderID=&quot;maincontent&quot;Runat=&quot;Server&quot;&gt;
&lt;divclass=&quot; col-md-12&quot;&gt;
&lt;divclass=&quot;card&quot;&gt;
&lt;%--Button For edit subject slect--%&gt;
&lt;divclass=&quot;btn-group bg-danger&quot;&gt;
&lt;asp:ButtonID=&quot;btn_panelsubjectlist&quot;runat=&quot;server&quot;Text=&quot;Edit Subject&quot;CssClass=&quot;btn btn-
info&quot;BorderStyle=&quot;None&quot;CausesValidation=&quot;False&quot;BackColor=&quot;#343A40&quot;/&gt;
&lt;/div&gt;
&lt;divclass=&quot;card-body&quot;&gt;
&lt;divclass=&quot;row form-group&quot;&gt;
&lt;labelclass=&quot;col-md-2 col-form-label &quot;&gt;Select Category&lt;/label&gt;
&lt;divclass=&quot;col-md-4&quot;&gt;
&lt;asp:DropDownListID=&quot;drp_categoryedit&quot;runat=&quot;server&quot;CssClass=&quot;form-
control&quot;DataTextField=&quot;category_name&quot;DataValueField=&quot;category_id&quot;&gt;
&lt;/asp:DropDownList&gt;
&lt;asp:RequiredFieldValidatorID=&quot;require_drpcategory&quot;runat=&quot;server&quot;ErrorMessage=&quot;You must select a
category&quot;ControlToValidate=&quot;drp_categoryedit&quot;ForeColor=&quot;red&quot;InitialValue=&quot;-1&quot;&gt;&lt;/asp:RequiredFieldValidator&gt;
&lt;/div&gt;
&lt;/div&gt;
&lt;divclass=&quot;row form-group&quot;&gt;
&lt;labelclass=&quot;col-md-2 col-form-label &quot;&gt;Subject Name&lt;/label&gt;
&lt;divclass=&quot;col-md-4&quot;&gt;
&lt;asp:TextBoxID=&quot;txt_subjectedit&quot;runat=&quot;server&quot;CssClass=&quot;form-control&quot;&gt;&lt;/asp:TextBox&gt;

72 | Page

&lt;asp:RequiredFieldValidatorID=&quot;require_subject&quot;runat=&quot;server&quot;ErrorMessage=&quot;Enter
subject&quot;ControlToValidate=&quot;txt_subjectedit&quot;ForeColor=&quot;red&quot;&gt;&lt;/asp:RequiredFieldValidator&gt;
&lt;/div&gt;
&lt;/div&gt;
&lt;divclass=&quot;card-footer&quot;&gt;
&lt;divclass=&quot;offset-2&quot;&gt;
&lt;asp:ButtonID=&quot;btn_editsubject&quot;runat=&quot;server&quot;Text=&quot;Edit
Subject&quot;CssClass=&quot;btn&quot;BackColor=&quot;#343A40&quot;BorderStyle=&quot;None&quot;ForeColor=&quot;White&quot;OnClick=&quot;btn_editsubject_
Click&quot;/&gt;
&lt;/div&gt;
&lt;asp:PanelID=&quot;panel_editsubject_warning&quot;runat=&quot;server&quot;Visible=&quot;false&quot;&gt;
&lt;br/&gt;
&lt;divclass=&quot;alert alert-danger text-center&quot;&gt;
&lt;asp:LabelID=&quot;lbl_editsubject_warning&quot;runat=&quot;server&quot;/&gt;
&lt;/div&gt;
&lt;/asp:Panel&gt;
&lt;/div&gt;
&lt;/div&gt;
&lt;/div&gt;
&lt;/div&gt;
&lt;/asp:Content&gt;
 Editsubject.aspx.cs
using System;
using System.Collections.Generic;
using System.Linq;
using System.Web;
using System.Web.UI;
using System.Web.UI.WebControls;
using System.Data.SqlClient;
using System.Data;
using System.Configuration;
publicpartialclassadmin_editsubject : System.Web.UI.Page
{
protectedvoid Page_Load(object sender, EventArgs e)
{
if (!IsPostBack)
{
string sid = Request.QueryString[&quot;sid&quot;];
if(sid == null)
{
Response.Redirect(&quot;~/admin/subject.aspx&quot;);
}
txt_subjectedit.Focus();
get_categorydrp(); // calling for dropdown method
categoryedit_fill(Convert.ToInt32(sid)); //calling for text method
}
}
protectedvoid btn_editsubject_Click(object sender, EventArgs e)
{
string sid = Request.QueryString[&quot;sid&quot;];
if (IsValid)
{
using(SqlConnection con = new SqlConnection(s))
{
SqlCommand cmd = new SqlCommand(&quot;spSubjectedit&quot;, con);

73 | Page

cmd.CommandType = CommandType.StoredProcedure;
cmd.Parameters.AddWithValue(&quot;@subject_name&quot;, txt_subjectedit.Text);
cmd.Parameters.AddWithValue(&quot;@subject_id&quot;, Convert.ToInt32(sid));
cmd.Parameters.AddWithValue(&quot;@category_id&quot;, drp_categoryedit.SelectedValue);
try
{
con.Open();
int i = (int)cmd.ExecuteNonQuery();
if (i &gt; 0)
{
Response.Redirect(&quot;~/admin/subject.aspx&quot;);
}
else
{
txt_subjectedit.Focus();
panel_editsubject_warning.Visible = true;
lbl_editsubject_warning.Text = &quot;Something went wrong. Can&#39;t update. Please try after sometime
later&lt;/br&gt; &quot;;
}
}
catch (Exception ex)
{
txt_subjectedit.Focus();
panel_editsubject_warning.Visible = true;
lbl_editsubject_warning.Text = &quot;Something went wrong. Please try after sometime later&lt;/br&gt; Contact
you developer for this problem&quot; + ex.Message;
}
} // end of using
}
else
{
txt_subjectedit.Focus();
panel_editsubject_warning.Visible = true;
lbl_editsubject_warning.Text = &quot;You must fill all the requirements&quot;;
}
}
string s = ConfigurationManager.ConnectionStrings[&quot;dbcs&quot;].ConnectionString;
//edit fill text method
publicvoid categoryedit_fill(int id)
{
using (SqlConnection con = new SqlConnection(s))
{
SqlCommand cmd = new SqlCommand(&quot;spSubjecteditfill&quot;, con);
cmd.CommandType = CommandType.StoredProcedure;
cmd.Parameters.AddWithValue(&quot;@id&quot;, id);
try
{
con.Open();
SqlDataReader rd = cmd.ExecuteReader();
while (rd.Read())
{
txt_subjectedit.Text = rd[&quot;subject_name&quot;].ToString();
}
}
catch (Exception ex)
{

74 | Page

panel_editsubject_warning.Visible = true;
lbl_editsubject_warning.Text = &quot;Something went wrong. Please try after sometime later&lt;/br&gt; Contact you
developer for this problem&quot; + ex.Message;
}
}
}
//edit fill dropdownmethod
publicvoid get_categorydrp()
{
using (SqlConnection con = new SqlConnection(s))
{
SqlCommand cmd = new SqlCommand(&quot;select * from category&quot;, con);
try
{
con.Open();
SqlDataReader rd = cmd.ExecuteReader();
drp_categoryedit.DataSource = rd;
drp_categoryedit.DataBind();
ListItem li = new ListItem(&quot;Select category&quot;, &quot;-1&quot;);
drp_categoryedit.Items.Insert(0, li);
}
catch (Exception ex)
{
txt_subjectedit.Focus();
panel_editsubject_warning.Visible = true;
lbl_editsubject_warning.Text = &quot;Something went wrong. Try again &lt;/br&gt;&quot; + ex.Message;
}
}
}
}
 Editexam.aspx
&lt;%@PageTitle=&quot;&quot;Language=&quot;C#&quot;MasterPageFile=&quot;~/admin.master&quot;AutoEventWireup=&quot;true&quot;CodeFile=&quot;editexam.
aspx.cs&quot;Inherits=&quot;editexam&quot;%&gt;
&lt;asp:ContentID=&quot;Content1&quot;ContentPlaceHolderID=&quot;headplaceholder&quot;runat=&quot;Server&quot;&gt;
&lt;/asp:Content&gt;
&lt;asp:ContentID=&quot;Content2&quot;ContentPlaceHolderID=&quot;maincontent&quot;runat=&quot;Server&quot;&gt;
&lt;divclass=&quot; col-md-12&quot;&gt;
&lt;divclass=&quot;card&quot;&gt;
&lt;%--Button For select edit--%&gt;
&lt;divclass=&quot;btn-group bg-danger&quot;&gt;
&lt;asp:ButtonID=&quot;btn_paneleditexam&quot;runat=&quot;server&quot;Text=&quot;Edit Exam&quot;CssClass=&quot;btn btn-
info&quot;BorderStyle=&quot;None&quot;CausesValidation=&quot;False&quot;BackColor=&quot;#343A40&quot;/&gt;
&lt;/div&gt;
&lt;%-- Edit exam --%&gt;
&lt;divclass=&quot;card-body&quot;&gt;
&lt;divclass=&quot;row form-group&quot;&gt;
&lt;labelclass=&quot;col-md-2 col-form-label &quot;&gt;Select Category&lt;/label&gt;
&lt;divclass=&quot;col-md-4&quot;&gt;
&lt;asp:DropDownListID=&quot;drp_editcategoryexam&quot;runat=&quot;server&quot;CssClass=&quot;form-
control&quot;DataTextField=&quot;category_name&quot;DataValueField=&quot;category_id&quot;&gt;
&lt;/asp:DropDownList&gt;
&lt;asp:RequiredFieldValidatorID=&quot;require_drpeditcategory&quot;runat=&quot;server&quot;ErrorMessage=&quot;You must select a
category&quot;ControlToValidate=&quot;drp_editcategoryexam&quot;ForeColor=&quot;red&quot;InitialValue=&quot;-
1&quot;SetFocusOnError=&quot;True&quot;&gt;&lt;/asp:RequiredFieldValidator&gt;
&lt;/div&gt;

75 | Page

&lt;/div&gt;
&lt;divclass=&quot;row form-group&quot;&gt;
&lt;labelclass=&quot;col-md-2 col-form-label &quot;&gt;Select Subject&lt;/label&gt;
&lt;divclass=&quot;col-md-4&quot;&gt;
&lt;asp:DropDownListID=&quot;drp_editsubjectexam&quot;runat=&quot;server&quot;CssClass=&quot;form-
control&quot;DataTextField=&quot;subject_name&quot;DataValueField=&quot;subject_id&quot;&gt;
&lt;/asp:DropDownList&gt;
&lt;asp:RequiredFieldValidatorID=&quot;require_editsubjecexam&quot;runat=&quot;server&quot;ErrorMessage=&quot;You must select a
subject&quot;ControlToValidate=&quot;drp_editsubjectexam&quot;ForeColor=&quot;red&quot;InitialValue=&quot;-
1&quot;SetFocusOnError=&quot;true&quot;&gt;&lt;/asp:RequiredFieldValidator&gt;
&lt;/div&gt;
&lt;/div&gt;
&lt;divclass=&quot;row form-group&quot;&gt;
&lt;labelclass=&quot;col-md-2 col-form-label &quot;&gt;Exam Name&lt;/label&gt;
&lt;divclass=&quot;col-md-4&quot;&gt;
&lt;asp:TextBoxID=&quot;txt_editexamname&quot;runat=&quot;server&quot;CssClass=&quot;form-control&quot;&gt;&lt;/asp:TextBox&gt;
&lt;asp:RequiredFieldValidatorID=&quot;require_editexamname&quot;runat=&quot;server&quot;ErrorMessage=&quot;Enter exam
name&quot;ControlToValidate=&quot;txt_editexamname&quot;ForeColor=&quot;red&quot;&gt;&lt;/asp:RequiredFieldValidator&gt;
&lt;/div&gt;
&lt;/div&gt;
&lt;divclass=&quot;row form-group&quot;&gt;
&lt;labelclass=&quot;col-md-2 col-form-label &quot;&gt;Exam Discription&lt;/label&gt;
&lt;divclass=&quot;col-md-9&quot;&gt;
&lt;asp:TextBoxID=&quot;txt_editexamdis&quot;runat=&quot;server&quot;TextMode=&quot;MultiLine&quot;CssClass=&quot;form-
control&quot;Height=&quot;150px&quot;&gt;&lt;/asp:TextBox&gt;
&lt;/div&gt;
&lt;/div&gt;
&lt;divclass=&quot;row form-group&quot;&gt;
&lt;labelclass=&quot;col-md-2 col-form-label &quot;&gt;Exam Date&lt;/label&gt;
&lt;divclass=&quot;col-md-4&quot;&gt;
&lt;asp:TextBoxID=&quot;txt_editexamdate&quot;runat=&quot;server&quot;CssClass=&quot;form-control&quot;TextMode=&quot;Date&quot;&gt;&lt;/asp:TextBox&gt;
&lt;asp:RequiredFieldValidatorID=&quot;require_editexamdate&quot;runat=&quot;server&quot;ErrorMessage=&quot;Enter exam
date&quot;ControlToValidate=&quot;txt_editexamdate&quot;ForeColor=&quot;red&quot;Display=&quot;Dynamic&quot;&gt;&lt;/asp:RequiredFieldValidator&gt;
&lt;/div&gt;
&lt;/div&gt;
&lt;divclass=&quot;row form-group&quot;&gt;
&lt;labelclass=&quot;col-md-2 col-form-label &quot;&gt;Exam Duration(Minute)&lt;/label&gt;
&lt;divclass=&quot;col-md-4&quot;&gt;
&lt;asp:TextBoxID=&quot;txt_editexamduration&quot;runat=&quot;server&quot;CssClass=&quot;form-
control&quot;TextMode=&quot;SingleLine&quot;&gt;&lt;/asp:TextBox&gt;
&lt;asp:RequiredFieldValidatorID=&quot;require_editexamduration&quot;runat=&quot;server&quot;ErrorMessage=&quot;Enter exam
duration&quot;ControlToValidate=&quot;txt_editexamduration&quot;ForeColor=&quot;red&quot;Display=&quot;Dynamic&quot;&gt;&lt;/asp:RequiredFieldVali
dator&gt;
&lt;asp:RegularExpressionValidatorID=&quot;requireregular_editexamduration&quot;runat=&quot;server&quot;ErrorMessage=&quot;Enter a valid
time&quot;ControlToValidate=&quot;txt_editexamduration&quot;ForeColor=&quot;red&quot;ValidationExpression=&quot;^\d{1,45}$&quot;Display=&quot;Dyn
amic&quot;&gt;&lt;/asp:RegularExpressionValidator&gt;
&lt;/div&gt;
&lt;/div&gt;
&lt;divclass=&quot;row form-group&quot;&gt;
&lt;labelclass=&quot;col-md-2 col-form-label &quot;&gt;Exam Pass Marks&lt;/label&gt;
&lt;divclass=&quot;col-md-4&quot;&gt;
&lt;asp:TextBoxID=&quot;txt_editpassexammarks&quot;runat=&quot;server&quot;CssClass=&quot;form-control&quot;&gt;&lt;/asp:TextBox&gt;
&lt;asp:RequiredFieldValidatorID=&quot;require_editpassexammark&quot;runat=&quot;server&quot;ErrorMessage=&quot;Enter exam
marks&quot;ControlToValidate=&quot;txt_editpassexammarks&quot;ForeColor=&quot;red&quot;Display=&quot;Dynamic&quot;&gt;&lt;/asp:RequiredFieldVali
dator&gt;

76 | Page
&lt;asp:RegularExpressionValidatorID=&quot;requireregular_editpassexammark&quot;runat=&quot;server&quot;ErrorMessage=&quot;Enter a
valid
marks&quot;ControlToValidate=&quot;txt_editpassexammarks&quot;ForeColor=&quot;red&quot;ValidationExpression=&quot;^\d{1,45}$&quot;Display=&quot;
Dynamic&quot;&gt;&lt;/asp:RegularExpressionValidator&gt;
&lt;/div&gt;
&lt;/div&gt;
&lt;divclass=&quot;row form-group&quot;&gt;
&lt;labelclass=&quot;col-md-2 col-form-label &quot;&gt;Exam Total Marks&lt;/label&gt;
&lt;divclass=&quot;col-md-4&quot;&gt;
&lt;asp:TextBoxID=&quot;txt_editexamtotalmarks&quot;runat=&quot;server&quot;CssClass=&quot;form-
control&quot;TextMode=&quot;SingleLine&quot;&gt;&lt;/asp:TextBox&gt;
&lt;asp:RequiredFieldValidatorID=&quot;require_editexammatotalmarks&quot;runat=&quot;server&quot;ErrorMessage=&quot;Enter exam total
marks&quot;ControlToValidate=&quot;txt_editpassexammarks&quot;ForeColor=&quot;red&quot;Display=&quot;Dynamic&quot;&gt;&lt;/asp:RequiredFieldVali
dator&gt;
&lt;asp:RegularExpressionValidatorID=&quot;reg_editexammatotalmarks&quot;runat=&quot;server&quot;ErrorMessage=&quot;Enter a valid
marks&quot;ControlToValidate=&quot;txt_editexamtotalmarks&quot;ForeColor=&quot;red&quot;ValidationExpression=&quot;^\d{1,45}$&quot;Display=&quot;
Dynamic&quot;&gt;&lt;/asp:RegularExpressionValidator&gt;
&lt;/div&gt;
&lt;/div&gt;
&lt;divclass=&quot;card-footer&quot;&gt;
&lt;divclass=&quot;offset-2&quot;&gt;
&lt;asp:ButtonID=&quot;btn_editexam&quot;runat=&quot;server&quot;Text=&quot;Edit
Exam&quot;CssClass=&quot;btn&quot;BackColor=&quot;#343A40&quot;BorderStyle=&quot;None&quot;ForeColor=&quot;White&quot;OnClick=&quot;btn_editexam_Clic
k&quot;/&gt;
&lt;/div&gt;
&lt;asp:PanelID=&quot;panel_editexam_warning&quot;runat=&quot;server&quot;Visible=&quot;false&quot;&gt;
&lt;br/&gt;
&lt;divclass=&quot;alert alert-danger text-center&quot;&gt;
&lt;asp:LabelID=&quot;lbl_exameditwarning&quot;runat=&quot;server&quot;/&gt;
&lt;/div&gt;
&lt;/asp:Panel&gt;
&lt;/div&gt;
&lt;/div&gt;
&lt;/div&gt;
&lt;/div&gt;
&lt;/asp:Content&gt;
 Editexam.aspx.cs
using System;
using System.Collections.Generic;
using System.Linq;
using System.Web;
using System.Web.UI;
using System.Web.UI.WebControls;
using System.Data.SqlClient;
using System.Data;
using System.Configuration;
publicpartialclasseditexam : System.Web.UI.Page
{
protectedvoid Page_Load(object sender, EventArgs e)
{
string eid = Request.QueryString[&quot;eid&quot;];
if (!IsPostBack)
{
if (eid == null)

77 | Page

{
Response.Redirect(&quot;~/admin/exam.aspx&quot;);
}
get_editexamfill(Convert.ToInt32(eid));
get_editcategorydrp();
get_editsubjectdrp();
}
}
string s = ConfigurationManager.ConnectionStrings[&quot;dbcs&quot;].ConnectionString;
//edit button to edit exam
protectedvoid btn_editexam_Click(object sender, EventArgs e)
{
string eid = Request.QueryString[&quot;eid&quot;];
if (IsValid)
{
string cs = ConfigurationManager.ConnectionStrings[&quot;dbcs&quot;].ConnectionString;
using (SqlConnection con = new SqlConnection(cs))
{
SqlCommand cmd = new SqlCommand(&quot;spEditexam&quot;, con);
cmd.CommandType = CommandType.StoredProcedure;
cmd.Parameters.AddWithValue(&quot;@examid&quot;, Convert.ToInt32(eid));
cmd.Parameters.AddWithValue(&quot;@examname&quot;, txt_editexamname.Text);
cmd.Parameters.AddWithValue(&quot;@examdiscription&quot;,txt_editexamdis.Text);
cmd.Parameters.AddWithValue(&quot;@examdate&quot;,txt_editexamdate.Text);
cmd.Parameters.AddWithValue(&quot;@examduration&quot;, txt_editexamduration.Text);
cmd.Parameters.AddWithValue(&quot;@exampassmarks&quot;, txt_editpassexammarks.Text);
cmd.Parameters.AddWithValue(&quot;@examnmarks&quot;, txt_editexamtotalmarks.Text);
cmd.Parameters.AddWithValue(&quot;@categoryfid&quot;, drp_editcategoryexam.SelectedValue);
cmd.Parameters.AddWithValue(&quot;@subjectfid&quot;, drp_editsubjectexam.SelectedValue);
try
{
con.Open();
int i = (int)cmd.ExecuteNonQuery();
if (i &gt; 0)
{
Response.Redirect(&quot;~/admin/exam.aspx&quot;);
}
else
{
txt_editexamname.Focus();
panel_editexam_warning.Visible = true;
lbl_exameditwarning.Text = &quot;Something went wrong. Can&#39;t update. Please try after sometime
later&lt;/br&gt; &quot;;
}
}
catch (Exception ex)
{
txt_editexamname.Focus();
panel_editexam_warning.Visible = true;
lbl_exameditwarning.Text = &quot;Something went wrong. Please try after sometime later&lt;/br&gt; Contact you
developer for this problem&quot; + ex.Message;
}
} // end of using
}
else
{

78 | Page

txt_editexamname.Focus();
panel_editexam_warning.Visible = true;
lbl_exameditwarning.Text = &quot;You must fill all the requirements&quot;;
}
}
//method for editfill
publicvoid get_editexamfill(int id)
{
using (SqlConnection con = new SqlConnection(s))
{
SqlCommand cmd = new SqlCommand(&quot;spEditexamfill&quot;, con);
cmd.CommandType = CommandType.StoredProcedure;
cmd.Parameters.AddWithValue(&quot;@examid&quot;, id);
try
{
con.Open();
SqlDataReader rd = cmd.ExecuteReader();
while (rd.Read())
{
txt_editexamname.Text = rd[&quot;exam_name&quot;].ToString();
txt_editexamdis.Text = rd[&quot;exam_description&quot;].ToString();
txt_editexamduration.Text = rd[&quot;exam_duration&quot;].ToString();
txt_editpassexammarks.Text = rd[&quot;exampass_marks&quot;].ToString();
txt_editexamtotalmarks.Text = rd[&quot;exam_marks&quot;].ToString();
}
}
catch (Exception ex)
{
panel_editexam_warning.Visible = true;
lbl_exameditwarning.Text = &quot;Something went wrong. Please try after sometime later&lt;/br&gt; Contact you
developer for this problem&quot; + ex.Message;
}
}
}
//method for category dropdown
publicvoid get_editcategorydrp()
{
using (SqlConnection con = new SqlConnection(s))
{
SqlCommand cmd = new SqlCommand(&quot;select * from category&quot;, con);
try
{
con.Open();
drp_editcategoryexam.DataSource = cmd.ExecuteReader();
drp_editcategoryexam.DataBind();
ListItem li = new ListItem(&quot;Select category&quot;, &quot;-1&quot;);
drp_editcategoryexam.Items.Insert(0, li);
}
catch (Exception ex)
{
txt_editexamname.Focus();
panel_editexam_warning.Visible = true;
lbl_exameditwarning.Text = &quot;Something went wrong. Try again &lt;/br&gt;&quot; + ex.Message;
}
}
}

79 | Page

//method for subject dropdown
publicvoid get_editsubjectdrp()
{
using (SqlConnection con = new SqlConnection(s))
{
SqlCommand cmd = new SqlCommand(&quot;select subject_id, subject_name from subject&quot;, con);
try
{
con.Open();
drp_editsubjectexam.DataSource = cmd.ExecuteReader();
drp_editsubjectexam.DataBind();
ListItem li = new ListItem(&quot;Select subject&quot;, &quot;-1&quot;);
drp_editsubjectexam.Items.Insert(0, li);
}
catch (Exception ex)
{
txt_editexamname.Focus();
panel_editexam_warning.Visible = true;
lbl_exameditwarning.Text = &quot;Something went wrong. Try again &lt;/br&gt;&quot; + ex.Message;
}
}
}
}
 Addquestion.aspx
&lt;%@PageTitle=&quot;&quot;Language=&quot;C#&quot;MasterPageFile=&quot;~/admin.master&quot;AutoEventWireup=&quot;true&quot;CodeFile=&quot;addquesti
on.aspx.cs&quot;Inherits=&quot;admin_addquestion&quot;%&gt;
&lt;asp:ContentID=&quot;Content1&quot;ContentPlaceHolderID=&quot;headplaceholder&quot;runat=&quot;Server&quot;&gt;
&lt;/asp:Content&gt;
&lt;asp:ContentID=&quot;Content2&quot;ContentPlaceHolderID=&quot;maincontent&quot;runat=&quot;Server&quot;&gt;
&lt;divclass=&quot;col-md-12&quot;&gt;
&lt;divclass=&quot;card&quot;&gt;
&lt;%--Button For select add question for exam--%&gt;
&lt;divclass=&quot;btn-group bg-danger&quot;&gt;
&lt;asp:ButtonID=&quot;btn_panelquestion&quot;runat=&quot;server&quot;Text=&quot;Add Question&quot;CssClass=&quot;btn btn-
info&quot;BorderStyle=&quot;None&quot;CausesValidation=&quot;False&quot;BackColor=&quot;#343A40&quot;/&gt;
&lt;/div&gt;
&lt;divclass=&quot;card-body&quot;&gt;
&lt;divclass=&quot;row form-group&quot;&gt;
&lt;labelclass=&quot;col-md-2 col-form-label &quot;&gt;Qusetion Name&lt;/label&gt;
&lt;divclass=&quot;col-md-9&quot;&gt;
&lt;asp:TextBoxID=&quot;txt_questionname&quot;runat=&quot;server&quot;TextMode=&quot;MultiLine&quot;CssClass=&quot;form-
control&quot;Height=&quot;150px&quot;&gt;&lt;/asp:TextBox&gt;
&lt;asp:RequiredFieldValidatorID=&quot;require_questionname&quot;runat=&quot;server&quot;ErrorMessage=&quot;Enter exam
name&quot;ControlToValidate=&quot;txt_questionname&quot;ForeColor=&quot;red&quot;&gt;&lt;/asp:RequiredFieldValidator&gt;
&lt;/div&gt;
&lt;/div&gt;
&lt;divclass=&quot;row form-group&quot;&gt;
&lt;labelclass=&quot;col-md-2 col-form-label &quot;&gt;Option A&lt;/label&gt;
&lt;divclass=&quot;col-md-9&quot;&gt;
&lt;asp:TextBoxID=&quot;txt_optionone&quot;runat=&quot;server&quot;CssClass=&quot;form-control&quot;&gt;&lt;/asp:TextBox&gt;
&lt;asp:RequiredFieldValidatorID=&quot;require_op1&quot;runat=&quot;server&quot;ErrorMessage=&quot;Enter option
one&quot;ControlToValidate=&quot;txt_optionone&quot;ForeColor=&quot;red&quot;&gt;&lt;/asp:RequiredFieldValidator&gt;
&lt;/div&gt;
&lt;/div&gt;

80 | Page

&lt;divclass=&quot;row form-group&quot;&gt;
&lt;labelclass=&quot;col-md-2 col-form-label &quot;&gt;Option B&lt;/label&gt;
&lt;divclass=&quot;col-md-9&quot;&gt;
&lt;asp:TextBoxID=&quot;txt_optiontwo&quot;runat=&quot;server&quot;CssClass=&quot;form-control&quot;&gt;&lt;/asp:TextBox&gt;
&lt;asp:RequiredFieldValidatorID=&quot;require_op2&quot;runat=&quot;server&quot;ErrorMessage=&quot;Enter option
two&quot;ControlToValidate=&quot;txt_optiontwo&quot;ForeColor=&quot;red&quot;&gt;&lt;/asp:RequiredFieldValidator&gt;
&lt;/div&gt;
&lt;/div&gt;
&lt;divclass=&quot;row form-group&quot;&gt;
&lt;labelclass=&quot;col-md-2 col-form-label &quot;&gt;Option C&lt;/label&gt;
&lt;divclass=&quot;col-md-9&quot;&gt;
&lt;asp:TextBoxID=&quot;txt_optionthree&quot;runat=&quot;server&quot;CssClass=&quot;form-control&quot;&gt;&lt;/asp:TextBox&gt;
&lt;asp:RequiredFieldValidatorID=&quot;require_op3&quot;runat=&quot;server&quot;ErrorMessage=&quot;Enter option
three&quot;ControlToValidate=&quot;txt_optionthree&quot;ForeColor=&quot;red&quot;&gt;&lt;/asp:RequiredFieldValidator&gt;
&lt;/div&gt;
&lt;/div&gt;
&lt;divclass=&quot;row form-group&quot;&gt;
&lt;labelclass=&quot;col-md-2 col-form-label &quot;&gt;Option D&lt;/label&gt;
&lt;divclass=&quot;col-md-9&quot;&gt;
&lt;asp:TextBoxID=&quot;txt_optionfour&quot;runat=&quot;server&quot;CssClass=&quot;form-control&quot;&gt;&lt;/asp:TextBox&gt;
&lt;asp:RequiredFieldValidatorID=&quot;require_op4&quot;runat=&quot;server&quot;ErrorMessage=&quot;Enter option
four&quot;ControlToValidate=&quot;txt_optionfour&quot;ForeColor=&quot;red&quot;&gt;&lt;/asp:RequiredFieldValidator&gt;
&lt;/div&gt;
&lt;/div&gt;
&lt;divclass=&quot;row form-group&quot;&gt;
&lt;labelclass=&quot;col-md-2 col-form-label text-center&quot;&gt;Correct Answer&lt;/label&gt;
&lt;divclass=&quot;col-md-4&quot;&gt;
&lt;asp:RadioButtonListID=&quot;rdo_correctanswer&quot;runat=&quot;server&quot;RepeatDirection=&quot;Horizontal&quot;RepeatLayout=&quot;Table&quot;C
ellPadding=&quot;10&quot;&gt;
&lt;asp:ListItemText=&quot;A&quot;Value=1&gt;&lt;/asp:ListItem&gt;
&lt;asp:ListItemText=&quot;B&quot;Value=2&gt;&lt;/asp:ListItem&gt;
&lt;asp:ListItemText=&quot;C&quot;Value=3&gt;&lt;/asp:ListItem&gt;
&lt;asp:ListItemText=&quot;D&quot;Value=4&gt;&lt;/asp:ListItem&gt;
&lt;/asp:RadioButtonList&gt;
&lt;asp:RequiredFieldValidatorID=&quot;req_rdo_correctanswer&quot;runat=&quot;server&quot;ErrorMessage=&quot;Select a correct
answer&quot;ControlToValidate=&quot;rdo_correctanswer&quot;ForeColor=&quot;red&quot;&gt;&lt;/asp:RequiredFieldValidator&gt;
&lt;/div&gt;
&lt;/div&gt;
&lt;divclass=&quot;card-footer&quot;&gt;
&lt;divclass=&quot;offset-2&quot;&gt;
&lt;asp:ButtonID=&quot;btn_addquestion&quot;runat=&quot;server&quot;Text=&quot;Add
Question&quot;CssClass=&quot;btn&quot;BackColor=&quot;#343A40&quot;BorderStyle=&quot;None&quot;ForeColor=&quot;White&quot;OnClick=&quot;btn_addquestio
n_Click&quot;/&gt;
&lt;/div&gt;
&lt;asp:PanelID=&quot;panel_addquestion_warning&quot;runat=&quot;server&quot;Visible=&quot;false&quot;&gt;
&lt;br/&gt;
&lt;divclass=&quot;alert alert-danger text-center&quot;&gt;
&lt;asp:LabelID=&quot;lbl_addquestionwarning&quot;runat=&quot;server&quot;/&gt;
&lt;/div&gt;
&lt;/asp:Panel&gt;
&lt;/div&gt;
&lt;/div&gt;
&lt;/div&gt;
&lt;/div&gt;
&lt;/asp:Content&gt;

81 | Page

 Addquestion.aspx.cs
using System;
using System.Collections.Generic;
using System.Linq;
using System.Web;
using System.Web.UI;
using System.Web.UI.WebControls;
using System.Data.SqlClient;
using System.Data;
using System.Configuration;
publicpartialclassadmin_addquestion : System.Web.UI.Page
{
protectedvoid Page_Load(object sender, EventArgs e)
{
if (!IsPostBack)
{
string eid = Request.QueryString[&quot;eid&quot;];
if (eid == null)
{
Response.Redirect(&quot;~/admin/exam.aspx&quot;);
}
}
}
string s = ConfigurationManager.ConnectionStrings[&quot;dbcs&quot;].ConnectionString; //string of connection
//for adding the question having exam id
protectedvoid btn_addquestion_Click(object sender, EventArgs e)
{
string eid = Request.QueryString[&quot;eid&quot;];
if (IsValid)
{
using (SqlConnection con = new SqlConnection(s))
{
SqlCommand cmd = new SqlCommand(&quot;spAddquestion&quot;, con);
cmd.CommandType = CommandType.StoredProcedure;
cmd.Parameters.AddWithValue(&quot;@questionname&quot;, txt_questionname.Text);
cmd.Parameters.AddWithValue(&quot;@optionone&quot;, txt_optionone.Text);
cmd.Parameters.AddWithValue(&quot;@optiontwo&quot;, txt_optiontwo.Text);
cmd.Parameters.AddWithValue(&quot;@optionthree&quot;, txt_optionthree.Text);
cmd.Parameters.AddWithValue(&quot;@optionfour&quot;, txt_optionfour.Text);
cmd.Parameters.AddWithValue(&quot;@questionanswer&quot;, rdo_correctanswer.SelectedValue);
cmd.Parameters.AddWithValue(&quot;@examfid&quot;, Convert.ToInt32(eid));
try
{
con.Open();
int i = cmd.ExecuteNonQuery();
if (i &gt; 0)
{
Response.Redirect(&quot;~/admin/exam.aspx&quot;);
}
else
{
txt_questionname.Focus();
panel_addquestion_warning.Visible = true;
lbl_addquestionwarning.Text = &quot;Try again. Subject is not added&quot;;
}
}

82 | Page

catch (Exception ex)
{
txt_questionname.Focus();
panel_addquestion_warning.Visible = true;
lbl_addquestionwarning.Text = &quot;Something went wrong. Subject is not added &lt;/br&gt;&quot; + ex.Message;
}
} //end of using
}
else
{
txt_questionname.Focus();
panel_addquestion_warning.Visible = true;
lbl_addquestionwarning.Text = &quot;You must fill all the requirements&quot;;
}
}
}
 Editquestion.aspx.cs
&lt;%@PageTitle=&quot;&quot;Language=&quot;C#&quot;MasterPageFile=&quot;~/admin.master&quot;AutoEventWireup=&quot;true&quot;CodeFile=&quot;editquesti
on.aspx.cs&quot;Inherits=&quot;admin_editquestion&quot;%&gt;
&lt;asp:ContentID=&quot;Content1&quot;ContentPlaceHolderID=&quot;headplaceholder&quot;Runat=&quot;Server&quot;&gt;
&lt;/asp:Content&gt;
&lt;asp:ContentID=&quot;Content2&quot;ContentPlaceHolderID=&quot;maincontent&quot;Runat=&quot;Server&quot;&gt;
&lt;divclass=&quot;col-md-12&quot;&gt;
&lt;divclass=&quot;card&quot;&gt;
&lt;%--Button For select add question for exam--%&gt;
&lt;divclass=&quot;btn-group bg-danger&quot;&gt;
&lt;asp:ButtonID=&quot;btn_paneleditquestion&quot;runat=&quot;server&quot;Text=&quot;Edit Question&quot;CssClass=&quot;btn btn-
info&quot;BorderStyle=&quot;None&quot;CausesValidation=&quot;False&quot;BackColor=&quot;#343A40&quot;/&gt;
&lt;/div&gt;
&lt;divclass=&quot;card-body&quot;&gt;
&lt;divclass=&quot;row form-group&quot;&gt;
&lt;labelclass=&quot;col-md-2 col-form-label &quot;&gt;Select Exam&lt;/label&gt;
&lt;divclass=&quot;col-md-4&quot;&gt;
&lt;asp:DropDownListID=&quot;drp_editexam&quot;runat=&quot;server&quot;CssClass=&quot;form-
control&quot;DataTextField=&quot;exam_name&quot;DataValueField=&quot;exam_id&quot;&gt;
&lt;/asp:DropDownList&gt;
&lt;asp:RequiredFieldValidatorID=&quot;require_editexam&quot;runat=&quot;server&quot;ErrorMessage=&quot;You must select a
exam&quot;ControlToValidate=&quot;drp_editexam&quot;ForeColor=&quot;red&quot;InitialValue=&quot;-
1&quot;SetFocusOnError=&quot;true&quot;&gt;&lt;/asp:RequiredFieldValidator&gt;
&lt;/div&gt;
&lt;/div&gt;
&lt;divclass=&quot;row form-group&quot;&gt;
&lt;labelclass=&quot;col-md-2 col-form-label &quot;&gt;Qusetion Name&lt;/label&gt;
&lt;divclass=&quot;col-md-9&quot;&gt;
&lt;asp:TextBoxID=&quot;txt_editquestionname&quot;runat=&quot;server&quot;TextMode=&quot;MultiLine&quot;CssClass=&quot;form-
control&quot;Height=&quot;150px&quot;&gt;&lt;/asp:TextBox&gt;
&lt;asp:RequiredFieldValidatorID=&quot;require_editquestionname&quot;runat=&quot;server&quot;ErrorMessage=&quot;Enter exam
name&quot;ControlToValidate=&quot;txt_editquestionname&quot;ForeColor=&quot;red&quot;&gt;&lt;/asp:RequiredFieldValidator&gt;
&lt;/div&gt;
&lt;/div&gt;
&lt;divclass=&quot;row form-group&quot;&gt;
&lt;labelclass=&quot;col-md-2 col-form-label &quot;&gt;Option A&lt;/label&gt;
&lt;divclass=&quot;col-md-9&quot;&gt;
&lt;asp:TextBoxID=&quot;txt_editoptionone&quot;runat=&quot;server&quot;CssClass=&quot;form-control&quot;&gt;&lt;/asp:TextBox&gt;

83 | Page

&lt;asp:RequiredFieldValidatorID=&quot;require_editop1&quot;runat=&quot;server&quot;ErrorMessage=&quot;Enter option
one&quot;ControlToValidate=&quot;txt_editoptionone&quot;ForeColor=&quot;red&quot;&gt;&lt;/asp:RequiredFieldValidator&gt;
&lt;/div&gt;
&lt;/div&gt;
&lt;divclass=&quot;row form-group&quot;&gt;
&lt;labelclass=&quot;col-md-2 col-form-label &quot;&gt;Option B&lt;/label&gt;
&lt;divclass=&quot;col-md-9&quot;&gt;
&lt;asp:TextBoxID=&quot;txt_editoptiontwo&quot;runat=&quot;server&quot;CssClass=&quot;form-control&quot;&gt;&lt;/asp:TextBox&gt;
&lt;asp:RequiredFieldValidatorID=&quot;require_editop2&quot;runat=&quot;server&quot;ErrorMessage=&quot;Enter option
two&quot;ControlToValidate=&quot;txt_editoptiontwo&quot;ForeColor=&quot;red&quot;&gt;&lt;/asp:RequiredFieldValidator&gt;
&lt;/div&gt;
&lt;/div&gt;
&lt;divclass=&quot;row form-group&quot;&gt;
&lt;labelclass=&quot;col-md-2 col-form-label &quot;&gt;Option C&lt;/label&gt;
&lt;divclass=&quot;col-md-9&quot;&gt;
&lt;asp:TextBoxID=&quot;txt_edtoptionthree&quot;runat=&quot;server&quot;CssClass=&quot;form-control&quot;&gt;&lt;/asp:TextBox&gt;
&lt;asp:RequiredFieldValidatorID=&quot;require_editop3&quot;runat=&quot;server&quot;ErrorMessage=&quot;Enter option
three&quot;ControlToValidate=&quot;txt_edtoptionthree&quot;ForeColor=&quot;red&quot;&gt;&lt;/asp:RequiredFieldValidator&gt;
&lt;/div&gt;
&lt;/div&gt;
&lt;divclass=&quot;row form-group&quot;&gt;
&lt;labelclass=&quot;col-md-2 col-form-label &quot;&gt;Option D&lt;/label&gt;
&lt;divclass=&quot;col-md-9&quot;&gt;
&lt;asp:TextBoxID=&quot;txt_editoptionfour&quot;runat=&quot;server&quot;CssClass=&quot;form-control&quot;&gt;&lt;/asp:TextBox&gt;
&lt;asp:RequiredFieldValidatorID=&quot;require_editop4&quot;runat=&quot;server&quot;ErrorMessage=&quot;Enter option
four&quot;ControlToValidate=&quot;txt_editoptionfour&quot;ForeColor=&quot;red&quot;&gt;&lt;/asp:RequiredFieldValidator&gt;
&lt;/div&gt;
&lt;/div&gt;
&lt;divclass=&quot;row form-group&quot;&gt;
&lt;labelclass=&quot;col-md-2 col-form-label text-center&quot;&gt;Correct Answer&lt;/label&gt;
&lt;divclass=&quot;col-md-4&quot;&gt;
&lt;asp:RadioButtonListID=&quot;rdo_editcorrectanswer&quot;runat=&quot;server&quot;RepeatDirection=&quot;Horizontal&quot;RepeatLayout=&quot;Tabl
e&quot;CellPadding=&quot;10&quot;&gt;
&lt;asp:ListItemText=&quot;A&quot;Value=1&gt;&lt;/asp:ListItem&gt;
&lt;asp:ListItemText=&quot;B&quot;Value=2&gt;&lt;/asp:ListItem&gt;
&lt;asp:ListItemText=&quot;C&quot;Value=3&gt;&lt;/asp:ListItem&gt;
&lt;asp:ListItemText=&quot;D&quot;Value=4&gt;&lt;/asp:ListItem&gt;
&lt;/asp:RadioButtonList&gt;
&lt;asp:RequiredFieldValidatorID=&quot;req_rdo_editcorrectanswer&quot;runat=&quot;server&quot;ErrorMessage=&quot;Select a correct
answer&quot;ControlToValidate=&quot;rdo_editcorrectanswer&quot;ForeColor=&quot;red&quot;&gt;&lt;/asp:RequiredFieldValidator&gt;
&lt;/div&gt;
&lt;/div&gt;
&lt;divclass=&quot;card-footer&quot;&gt;
&lt;divclass=&quot;offset-2&quot;&gt;
&lt;asp:ButtonID=&quot;btn_editquestion&quot;runat=&quot;server&quot;Text=&quot;Edit
Question&quot;CssClass=&quot;btn&quot;BackColor=&quot;#343A40&quot;BorderStyle=&quot;None&quot;ForeColor=&quot;White&quot;OnClick=&quot;btn_editquestio
n_Click&quot;/&gt;
&lt;/div&gt;
&lt;asp:PanelID=&quot;panel_editquestion_warning&quot;runat=&quot;server&quot;Visible=&quot;false&quot;&gt;
&lt;br/&gt;
&lt;divclass=&quot;alert alert-danger text-center&quot;&gt;
&lt;asp:LabelID=&quot;lbl_editquestionwarning&quot;runat=&quot;server&quot;/&gt;
&lt;/div&gt;
&lt;/asp:Panel&gt;
&lt;/div&gt;
&lt;/div&gt;

84 | Page

&lt;/div&gt;
&lt;/div&gt;
&lt;/asp:Content&gt;
 Editquestion.aspx.cs
using System;
using System.Collections.Generic;
using System.Linq;
using System.Web;
using System.Web.UI;
using System.Web.UI.WebControls;
using System.Data.SqlClient;
using System.Data;
using System.Configuration;
publicpartialclassadmin_addquestion : System.Web.UI.Page
{
protectedvoid Page_Load(object sender, EventArgs e)
{
if (!IsPostBack)
{
string eid = Request.QueryString[&quot;eid&quot;];
if (eid == null)
{
Response.Redirect(&quot;~/admin/exam.aspx&quot;);
}
}
}
string s = ConfigurationManager.ConnectionStrings[&quot;dbcs&quot;].ConnectionString; //string of connection
//for adding the question having exam id
protectedvoid btn_addquestion_Click(object sender, EventArgs e)
{
string eid = Request.QueryString[&quot;eid&quot;];
if (IsValid)
{
using (SqlConnection con = new SqlConnection(s))
{
SqlCommand cmd = new SqlCommand(&quot;spAddquestion&quot;, con);
cmd.CommandType = CommandType.StoredProcedure;
cmd.Parameters.AddWithValue(&quot;@questionname&quot;, txt_questionname.Text);
cmd.Parameters.AddWithValue(&quot;@optionone&quot;, txt_optionone.Text);
cmd.Parameters.AddWithValue(&quot;@optiontwo&quot;, txt_optiontwo.Text);
cmd.Parameters.AddWithValue(&quot;@optionthree&quot;, txt_optionthree.Text);
cmd.Parameters.AddWithValue(&quot;@optionfour&quot;, txt_optionfour.Text);
cmd.Parameters.AddWithValue(&quot;@questionanswer&quot;, rdo_correctanswer.SelectedValue);
cmd.Parameters.AddWithValue(&quot;@examfid&quot;, Convert.ToInt32(eid));
try
{
con.Open();
int i = cmd.ExecuteNonQuery();
if (i &gt; 0)
{
Response.Redirect(&quot;~/admin/exam.aspx&quot;);
}
else

85 | Page

{
txt_questionname.Focus();
panel_addquestion_warning.Visible = true;
lbl_addquestionwarning.Text = &quot;Try again. Subject is not added&quot;;
}
}
catch (Exception ex)
{
txt_questionname.Focus();
panel_addquestion_warning.Visible = true;
lbl_addquestionwarning.Text = &quot;Something went wrong. Subject is not added &lt;/br&gt;&quot; + ex.Message;
}
} //end of using
}
else
{
txt_questionname.Focus();
panel_addquestion_warning.Visible = true;
lbl_addquestionwarning.Text = &quot;You must fill all the requirements&quot;;
} } }
