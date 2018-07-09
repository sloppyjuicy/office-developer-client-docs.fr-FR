---
title: Utilisation des Classes XPathNavigator et XPathNodeIterator
manager: soliver
ms.date: 12/07/2015
ms.audience: Developer
keywords:
- xpathnodeiterator class [infopath 2007],XPathNavigator class [InfoPath 2007],form XML data [InfoPath 2007], accessing,XML DOM [InfoPath 2007],converting MSXML5 script [InfoPath 2007],MSXML5 script [InfoPath 2007], converting
localization_priority: Normal
ms.assetid: 72fb3ee5-f18e-4f9c-adc6-698ac037b79d
description: Pour accéder aux données XML dans les sources de données du modèle de formulaire et les manipuler, un grand nombre de membres du modèle objet avec code managé fourni par l'espace de noms Microsoft.Office.InfoPath créent ou se voient attribuer une instance de la classe XPathNavigator de l'espace de noms System.Xml.XPath. Après avoir accédé à un objet XPathNavigator retourné par un membre du modèle objet InfoPath, vous pouvez utiliser les propriétés et les méthodes de la classe XPathNavigator pour travailler avec les données.
ms.openlocfilehash: a672ea2733d971c829b77e0c18a74f26c7050b34
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19782402"
---
# <a name="work-with-the-xpathnavigator-and-xpathnodeiterator-classes"></a><span data-ttu-id="d5ad1-105">Utilisation des Classes XPathNavigator et XPathNodeIterator</span><span class="sxs-lookup"><span data-stu-id="d5ad1-105">Work with the XPathNavigator and XPathNodeIterator Classes</span></span>

<span data-ttu-id="d5ad1-p102">Pour accéder aux données XML dans les sources de données du modèle de formulaire et les manipuler, un grand nombre de membres du modèle objet avec code managé fourni par l'espace de noms [Microsoft.Office.InfoPath](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.aspx) créent ou se voient attribuer une instance de la classe **XPathNavigator** de l'espace de noms **System.Xml.XPath**. Après avoir accédé à un objet **XPathNavigator** retourné par un membre du modèle objet InfoPath, vous pouvez utiliser les propriétés et les méthodes de la classe **XPathNavigator** pour travailler avec les données.</span><span class="sxs-lookup"><span data-stu-id="d5ad1-p102">To access and manipulate the XML data in form template data sources, many members of the managed code object model provided by the [Microsoft.Office.InfoPath](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.aspx) namespace either create or can be passed an instance of the **XPathNavigator** class of the **System.Xml.XPath** namespace. After you have access to an **XPathNavigator** object returned by an InfoPath object model member, you can use the properties and methods of the **XPathNavigator** class to work with the data.</span></span> 
  
<span data-ttu-id="d5ad1-p103">Le membre le plus couramment utilisé de l'espace de noms **Microsoft.Office.InfoPath** qui utilise la classe **XPathNavigator** est la méthode [CreateNavigator](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSource.CreateNavigator.aspx) de la classe [DataSource](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSource.aspx) qui vous permet d'utiliser les données stockées représentées par un objet **DataSource**. La méthode **CreateNavigator** crée un objet **XPathNavigator** placé à la racine de la source de données représentée par l'objet **DataSource**.</span><span class="sxs-lookup"><span data-stu-id="d5ad1-p103">The most frequently used member of the **Microsoft.Office.InfoPath** namespace that uses the **XPathNavigator** class is the [CreateNavigator](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSource.CreateNavigator.aspx) method of the [DataSource](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSource.aspx) class, which enables you to work with the stored data represented by a **DataSource** object. The **CreateNavigator** method creates an **XPathNavigator** object positioned at the root of the data source represented by the **DataSource** object.</span></span> 
  
> [!TIP]
> <span data-ttu-id="d5ad1-110">Si vous avez l'habitude d'utiliser MSXML5 à partir du script pour travailler avec des données dans Microsoft InfoPath 2003, vous pouvez considérer la méthode **CreateNavigator** en remplacement de la propriété **DOM** de l'objet **DataObject**.</span><span class="sxs-lookup"><span data-stu-id="d5ad1-110">If you are familiar with using MSXML5 from script to work with data in Microsoft InfoPath 2003, you can think of the **CreateNavigator** method as the replacement for the **DOM** property of the **DataObject**.</span></span> 
  
## <a name="using-the-xpathnavigator-class-to-access-the-main-data-source-of-the-form"></a><span data-ttu-id="d5ad1-111">Utilisation de la classe XPathNavigator pour accéder à la source principale de données du formulaire</span><span class="sxs-lookup"><span data-stu-id="d5ad1-111">Using the XPathNavigator Class to Access the Main Data Source of the Form</span></span>

<span data-ttu-id="d5ad1-p104">Pour accéder à la source de données principale du formulaire, appelez la méthode [CreateNavigator](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSource.CreateNavigator.aspx) directement depuis le mot clé **this** (C#) ou **Me** (Visual Basic). L'exemple suivant crée un objet **XPathNavigator** placé à la racine de la source de données principale à l'aide de la méthode **CreateNavigator**, puis utilise la propriété **OuterXml** de la classe **XPathNavigator** pour afficher le code XML retourné dans une zone de message.</span><span class="sxs-lookup"><span data-stu-id="d5ad1-p104">To access the main data source of the form, call the [CreateNavigator](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSource.CreateNavigator.aspx) method directly from the **this** (C#) or **Me** (Visual Basic) keyword. The following example creates an **XPathNavigator** object positioned at the root of the main data source by using the **CreateNavigator** method, and then uses the **OuterXml** property of the **XPathNavigator** class to display the XML returned in a message box.</span></span> 
  
```cs
XPathNavigator myNavigator = 
   this.CreateNavigator();
MessageBox.Show("Main data source XML: " +
   myNavigator.OuterXml.ToString());
```

```vb
Dim myNavigator As XPathNavigator  = _
   Me.CreateNavigator()
MessageBox.Show("Main data source XML: " &amp; _
   myNavigator.OuterXml.ToString())
```

> [!NOTE]
> <span data-ttu-id="d5ad1-114">L'appel à la méthode [CreateNavigator](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSource.CreateNavigator.aspx) directement depuis le mot clé **this** ou **Me** équivaut à appeler la méthode [CreateNavigator](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSource.CreateNavigator.aspx) à l'aide de la propriété [MainDataSource](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.MainDataSource.aspx) (  `this.MainDataSource.CreateNavigator()`) ou à passer une chaîne vide à la propriété [DataSources](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.DataSources.aspx) de la classe [XmlForm](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.aspx) (  `this.DataSources[""].CreateNavigator()`).</span><span class="sxs-lookup"><span data-stu-id="d5ad1-114">Calling the [CreateNavigator](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSource.CreateNavigator.aspx) method directly from the **this** or **Me** keyword is equivalent to calling [CreateNavigator](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSource.CreateNavigator.aspx) method by using the [MainDataSource](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.MainDataSource.aspx) property (  `this.MainDataSource.CreateNavigator()`) or by passing an empty string to the [DataSources](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.DataSources.aspx) property of the [XmlForm](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.aspx) class (  `this.DataSources[""].CreateNavigator()`).</span></span> 
  
## <a name="selecting-and-setting-the-xml-nodes-for-fields-in-the-main-data-source"></a><span data-ttu-id="d5ad1-115">Sélection et définition de nœuds XML pour les champs de la source de données principale</span><span class="sxs-lookup"><span data-stu-id="d5ad1-115">Selecting and Setting the XML Nodes for Fields in the Main Data Source</span></span>
<span data-ttu-id="d5ad1-116"><a name="InfoPath2007XPathNavigatorClassFormTemplates_SelectingXMLNodes"> </a></span><span class="sxs-lookup"><span data-stu-id="d5ad1-116"></span></span>

<span data-ttu-id="d5ad1-p105">Pour sélectionner un nœud XML unique pour champ de la source de données, utilisez la méthode **SelectSingleNode(String,IXmlNamespaceResolver)** de la classe **XPathNavigator**. Si vous voulez utiliser un jeu de champs récurrents ou de groupes récurrents, utilisez la méthode **Select(String,IXmlNamespaceResolver)** de la classe **XPathNavigator**. Cette méthode retourne un objet **XPathNodeIterator** qui représente une collection de nœuds.</span><span class="sxs-lookup"><span data-stu-id="d5ad1-p105">To select the single XML node for a field in a data source, use the **SelectSingleNode(String,IXmlNamespaceResolver)** method of the **XPathNavigator** class. If you want to work with a set of repeating fields or repeating groups, use the **Select(String,IXmlNamespaceResolver)** method of the **XPathNavigator** class. This method returns an **XPathNodeIterator** object that represents a collection of nodes.</span></span> 
  
### <a name="selecting-and-setting-the-value-of-a-single-node"></a><span data-ttu-id="d5ad1-120">Sélection et définition de la valeur d'un nœud unique</span><span class="sxs-lookup"><span data-stu-id="d5ad1-120">Selecting and Setting the Value of a Single Node</span></span>

<span data-ttu-id="d5ad1-p106">La méthode surchargée **SelectSingleNode** que vous devez utiliser comprend un paramètre  _xpath_ qui prend une expression XPath sous forme de chaîne et un paramètre  _resolver_ qui prend l'objet **XmlNamespaceManager** pour résoudre les préfixes d'espaces de noms. Pour sélectionner un nœud unique dans la source de données principale du formulaire, transmettez une expression XPath qui spécifie le champ ou groupe que vous voulez sélectionner pour le paramètre  _xpath_, avec l'objet **XmlNamespaceManager** qui est retourné par la propriété [NamespaceManager](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.NamespaceManager.aspx) de l'objet **XmlForm**. L'objet **XmlNamespaceManager** retourné est initialisé lors du chargement avec tous les espaces de noms définis par le fichier de définition de formulaire du modèle de formulaire (.xsf).</span><span class="sxs-lookup"><span data-stu-id="d5ad1-p106">The overloaded **SelectSingleNode** method that you must use has an  _xpath_ parameter that takes an XPath expression as a string, and a  _resolver_ parameter that takes an **XmlNamespaceManager** object for resolving namespace prefixes. To select a single node in the form's main data source, pass in an XPath expression that specifies the field or group that you want to select for the  _xpath_ parameter, together with the **XmlNamespaceManager** object that is returned by the [NamespaceManager](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.NamespaceManager.aspx) property of the **XmlForm** object. The returned **XmlNamespaceManager** object is initialized at load time with all the namespaces that are defined by the form template's form definition file (.xsf).</span></span> 
  
> [!TIP]
> <span data-ttu-id="d5ad1-p107">La façon la plus simple de créer une expression XPath pour sélectionner un nœud dans la source de données du formulaire est de cliquer avec le bouton droit sur le champ ou sur le groupe dans le volet Office **Champs**, puis de cliquer sur **Copier XPath**. Pour créer et tester des expressions XPath modifiées manuellement pour accéder à des nœuds dans un schéma XML complexe ou fortement imbriqué, ajoutez un contrôle **Zone d'expression** au formulaire, spécifiez l'expression XPath du contrôle, puis affichez l'aperçu du formulaire pour afficher les résultats.</span><span class="sxs-lookup"><span data-stu-id="d5ad1-p107">The easiest way to create an XPath expression for selecting a node in the form's data source is to right-click the field or group in the **Fields** task pane, and then click **Copy XPath**. To create and test hand-edited XPath expressions for accessing nodes in a complex or heavily nested XML schema, add an **Expression Box** control to the form, specify the XPath expression for the control, and then preview the form to display the results.</span></span> 
  
<span data-ttu-id="d5ad1-p108">L'exemple qui suit utilise la méthode **SelectSingleNode** pour sélectionner le nœud unique du champ  `EmailAlias`. Il utilise ensuite la méthode **SetValue** de la classe **XPathNavigator** et la propriété [UserName](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.User.UserName.aspx) de la classe [User](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.User.aspx) pour définir la valeur du champ sur celle de l'alias de l'utilisateur actuel.</span><span class="sxs-lookup"><span data-stu-id="d5ad1-p108">The following example uses the **SelectSingleNode** method to select the single node for the  `EmailAlias` field. Then it uses the **SetValue** method of the **XPathNavigator** class and the [UserName](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.User.UserName.aspx) property of the [User](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.User.aspx) class to set the value of the field to the current user's alias.</span></span> 
  
```cs
XPathNavigator emailAlias = 
   this.CreateNavigator().SelectSingleNode(
      "/my:myFields/my:EmailAlias", NamespaceManager);
emailAlias.SetValue(this.Application.User.UserName.ToString());
```

```vb
Dim emailAlias As XPathNavigator = _
   Me.CreateNavigator().SelectSingleNode( _
      "/my:myFields/my:EmailAlias", NamespaceManager)
emailAlias.SetValue(Me.Application.User.UserName.ToString())
```

<span data-ttu-id="d5ad1-128">Pour plus d’informations sur la façon de créer des expressions XPath, voir la XPath référence sur MSDN, ainsi que le [langage XML Path (XPath) Version 1.0 W3C recommandation](http://www.w3.org/TR/xpath).</span><span class="sxs-lookup"><span data-stu-id="d5ad1-128">For information about how to create XPath expressions, see the XPath Reference on MSDN, and the [XML Path Language (XPath) Version 1.0 W3C Recommendation](http://www.w3.org/TR/xpath).</span></span>
  
### <a name="setting-the-value-of-a-node-that-has-the-xsinil-attribute"></a><span data-ttu-id="d5ad1-129">Définition de la valeur d'un nœud qui possède l'attribut xsi:nil</span><span class="sxs-lookup"><span data-stu-id="d5ad1-129">Setting the Value of a Node That Has the xsi:nil Attribute</span></span>

<span data-ttu-id="d5ad1-p109">Pour certains types de données, le fait de définir une valeur nulle par programme génère l'erreur « La validation de schéma a détecté des erreurs qui ne concernent pas le type de données ». En général, la cause de cette erreur est que l'attribut [xsi:nil](http://www.w3.org/TR/2001/REC-xmlschema-1-20010502/#xsi_nil) de l'élément est défini sur **true**. Si vous examinez l'élément XML sous-jacent du champ vierge du formulaire, vous verrez ce paramètre. Par exemple, l'attribut **xsi:nil** du fragment XML du champ Date vierge suivant est défini sur **true**.</span><span class="sxs-lookup"><span data-stu-id="d5ad1-p109">For certain data types, trying to set the value of a blank field programmatically raises the error "Schema validation found non-data type errors." Typically the cause of this error is that the element has the [xsi:nil](http://www.w3.org/TR/2001/REC-xmlschema-1-20010502/#xsi_nil) attribute set to **true**. If you examine the underlying XML element for the blank field in the form, you can see this setting. For example, the XML fragment for the following blank Date field has the **xsi:nil** attribute set to **true**.</span></span>
  
```XML
<my:myDate xsi:nil="true"></my:myDate>
```

<span data-ttu-id="d5ad1-p110">Si l'attribut **xsi:nil** est défini sur **true**, il indique que l'élément est présent mais n'a pas de valeur, en d'autres termes est null. Si vous essayez de définir la valeur d'un tel nœud par programme, InfoPath affiche l'erreur « La validation de schéma a détecté des erreurs qui ne concernent pas le type de données. », car l'élément est signalé comme null. InfoPath définit l'attribut **xsi:nil** sur **true** pour les champs null des types de données suivants :</span><span class="sxs-lookup"><span data-stu-id="d5ad1-p110">If the **xsi:nil** attribute is set to **true**, it indicates that the element is present but has no value, or in other words, is null . If you try to programmatically set the value of such a node, InfoPath displays the "Schema validation found non-data type errors" message because the element is currently flagged as being null . InfoPath sets the **xsi:nil** attribute to **true** for null fields of the following data types:</span></span> 
  
- <span data-ttu-id="d5ad1-137">**Whole Number (integer)**</span><span class="sxs-lookup"><span data-stu-id="d5ad1-137">**Whole Number (integer)**</span></span>
    
- <span data-ttu-id="d5ad1-138">**Decimal (double)**</span><span class="sxs-lookup"><span data-stu-id="d5ad1-138">**Decimal (double)**</span></span>
    
- <span data-ttu-id="d5ad1-139">**Date (date)**</span><span class="sxs-lookup"><span data-stu-id="d5ad1-139">**Date (date)**</span></span>
    
- <span data-ttu-id="d5ad1-140">**Time (time)**</span><span class="sxs-lookup"><span data-stu-id="d5ad1-140">**Time (time)**</span></span>
    
- <span data-ttu-id="d5ad1-141">**Date and Time (dateTime)**</span><span class="sxs-lookup"><span data-stu-id="d5ad1-141">**Date and Time (dateTime)**</span></span>
    
<span data-ttu-id="d5ad1-p111">Pour empêcher cette erreur, votre code doit rechercher la présence de l'attribut **xsi:nil**. S'il est présent, supprimez-le avant de définir la valeur du nœud. La sous-routine qui suit prend un objet **XpathNavigator** placé sur le nœud que vous souhaitez définir, recherche l'attribut **nil** et le supprime s'il existe.</span><span class="sxs-lookup"><span data-stu-id="d5ad1-p111">To prevent this error, your code must test for the **xsi:nil** attribute, and if it is present, remove it before setting the value of the node. The following subroutine takes an **XpathNavigator** object positioned on the node that you want to set, checks for the **nil** attribute, and then deletes it, if it exists.</span></span> 
  
```cs
public void DeleteNil(XPathNavigator node)
{
   if (node.MoveToAttribute(
      "nil", "http://www.w3.org/2001/XMLSchema-instance"))
      node.DeleteSelf();
}
```

```vb
Public Sub DeleteNil(ByVal node As XPathNavigator)
   If (node.MoveToAttribute( _
      "nil", "http://www.w3.org/2001/XMLSchema-instance")) Then
      node.DeleteSelf()
   End If
End Sub
```

<span data-ttu-id="d5ad1-144">Vous pouvez appeler cette sous-routine avant d'essayer de définir un champ d'un type de données qui peut avoir l'attribut **xsi:nil**, comme présenté dans l'exemple ci-dessous, qui définit un champ Date.</span><span class="sxs-lookup"><span data-stu-id="d5ad1-144">You can call this subroutine before you try to set a field of a data type that might have the **xsi:nil** attribute, as shown in the following example that sets a Date field.</span></span> 
  
```cs
// Access the main data source.
XPathNavigator myForm = this.CreateNavigator();
// Select the field.
XPathNavigator myDate = myForm.SelectSingleNode("/my:myFields/my:myDate", NamespaceManager);
// Check for and remove the "nil" attribute.
DeleteNil(myDate);
// Build the current date in the proper format. (yyyy-mm-dd)
string curDate = DateTime.Today.Year + "-" + DateTime.Today.Month + 
   "-" + DateTime.Today.Day;
// Set the value of the myDate field.
myDate.SetValue(strCurDate);
```

```vb
' Access the main data source.
Dim myForm As XPathNavigator = Me.CreateNavigator()
' Select the field.
Dim myDate As XPathNavigator = _
   myForm.SelectSingleNode("/my:myFields/my:myDate", NamespaceManager)
' Check for and remove the "nil" attribute.
DeleteNil(myDate)
' Build the current date in the proper format. (yyyy-mm-dd)
Dim curDate As String = DateTime.Today.Year + "-" + _
   DateTime.Today.Month + "-" + DateTime.Today.Day
' Set the value of the myDate field.
myDate.SetValue(strCurDate)
```

> [!NOTE]
> <span data-ttu-id="d5ad1-p112">Bien que l'implémentation de l'objet **XPathNavigator** dans InfoPath expose la méthode **SetTypedValue**, qui est utilisée pour définir un nœud à l'aide d'une valeur de type spécifique, InforPath n'utilise pas cette méthode. Vous devez utiliser la méthode **SetValue**, et transmettre une valeur de chaîne au format correct pour le type de données du nœud.</span><span class="sxs-lookup"><span data-stu-id="d5ad1-p112">Although the implementation of the **XPathNavigator** object in InfoPath exposes the **SetTypedValue** method—which is used to set a node using a value of a specific type—InfoPath does not implement that method. You must use the **SetValue** method instead, and pass a string value of the correct format for the data type of the node.</span></span> 
  
### <a name="selecting-and-setting-a-set-of-repeating-nodes"></a><span data-ttu-id="d5ad1-147">Sélection et définition d'un jeu de nœuds récurrents</span><span class="sxs-lookup"><span data-stu-id="d5ad1-147">Selecting and Setting a Set of Repeating Nodes</span></span>

<span data-ttu-id="d5ad1-148">Pour spécifier des champs ou des groupes récurrents dont le nombre n'est pas déterminé, utilisez la méthode **Select** de la classe **XPathNavigator**.</span><span class="sxs-lookup"><span data-stu-id="d5ad1-148">To specify a set of repeating fields or groups that are of an indeterminate number, use the **Select** method of the **XPathNavigator** class.</span></span> <span data-ttu-id="d5ad1-149">Cette méthode renvoie un objet XPathNodeIterator que vous pouvez utiliser pour itérer la collection de nœuds spécifiée.</span><span class="sxs-lookup"><span data-stu-id="d5ad1-149">This method returns an XPathNodeIterator object that you can use to iterate over the specified collection of nodes.</span></span> 
  
<span data-ttu-id="d5ad1-150">Dans l'exemple suivant, votre modèle de formulaire contient une **Liste à puces** ou un autre contrôle récurrent qui est lié à un élément récurrent appelé  `field1`.</span><span class="sxs-lookup"><span data-stu-id="d5ad1-150">The following example assumes that your form template contains a **Bulleted List** or similar repeating control that is bound to a repeating element named  `field1`.</span></span> <span data-ttu-id="d5ad1-151">Le XPath de ce champ est transmis à la méthode **Select** et la valeur **XPathNodeIterator** retournée est affectée à la variable  `nodes`.</span><span class="sxs-lookup"><span data-stu-id="d5ad1-151">The XPath of the field is passed to the **Select** method, and the returned **XPathNodeIterator** is assigned to the  `nodes` variable.</span></span> <span data-ttu-id="d5ad1-152">Vous utilisez la méthode MoveNext pour itérer la collection de nœuds et la propriété en cours pour renvoyer un objet **XPathNavigator** placé sur le nœud actuel.</span><span class="sxs-lookup"><span data-stu-id="d5ad1-152">You use the MoveNext method to iterate over the collection of nodes, and the Current property to return an **XPathNavigator** object positioned on the current node.</span></span> <span data-ttu-id="d5ad1-153">Enfin, utilisez la propriété **Value** pour extraire et afficher la valeur de chaque champ extensible.</span><span class="sxs-lookup"><span data-stu-id="d5ad1-153">Finally, use the **Value** property to retrieve and display the value of each repeating field.</span></span> 
  
```cs
string message = String.Empty;
XPathNavigator root = this.CreateNavigator();
XPathNodeIterator nodes = 
   root.Select("/my:myFields/my:group1/my:field1", NamespaceManager);
while (nodes.MoveNext())
{
    message += nodes.Current.Value + System.Environment.NewLine;
}
MessageBox.Show(message);
```

```vb
Dim message As String = String.Empty
Dim root As XPathNavigator = Me.CreateNavigator()
Dim nodes As XPathNodeIterator = _
   root.Select("/my:myFields/my:group1/my:field1", NamespaceManager)
Do While nodes.MoveNext
    message += nodes.Current.Value &amp; System.Environment.NewLine
Loop
MessageBox.Show(message)
```

<span data-ttu-id="d5ad1-p115">L'exemple qui précède fonctionne avec des valeurs de chaîne dans le champ récurrent spécifié. Cependant, si ce champ contient des valeurs numériques, vous pouvez utiliser un code similaire pour parcourir les valeurs du champ et effectuer des opération, par exemple le calcul du total ou de la moyenne des valeurs.</span><span class="sxs-lookup"><span data-stu-id="d5ad1-p115">The previous example works with string values in the specified repeating field. However, if the field contains numeric values, you can use similar code to iterate over the values in the field to perform arithmetic, such as calculating the total or average of the values.</span></span>
  
<span data-ttu-id="d5ad1-156">De même, plutôt que d'utiliser la propriété **Value** pour récupérer la valeur de chaque instance du champ récurrent, vous pouvez utiliser la méthode **SetValue** pour parcourir les champs et en définir les valeurs, comme illustré dans l'exemple qui suit.</span><span class="sxs-lookup"><span data-stu-id="d5ad1-156">Similarly, instead of using the **Value** property to retrieve the value of each instance of the repeating field, you can use the **SetValue** method to iterate over the fields and set their values, as shown in the following example.</span></span> 
  
```cs
XPathNavigator root = this.CreateNavigator();
XPathNodeIterator nodes = 
   root.Select("/my:myFields/my:group1/my:field1", NamespaceManager);
int myInt = 1;
while (nodes.MoveNext())
{
   nodes.Current.SetValue(myInt.ToString());
   myInt = myInt + 1;
}
```

```vb
Dim root As XPathNavigator = Me.CreateNavigator()
Dim nodes As XPathNodeIterator = _
   root.Select("/my:myFields/my:group1/my:field1", NamespaceManager)
Dim myInt As Integer = 1
Do While nodes.MoveNext
   nodes.Current.SetValue(myInt.ToString())
   myInt = myInt + 1
Loop
```

## <a name="using-the-xpathnavigator-class-to-access-an-external-data-source"></a><span data-ttu-id="d5ad1-157">Utilisation de la classe XPathNavigator pour accéder à une source de données externe</span><span class="sxs-lookup"><span data-stu-id="d5ad1-157">Using the XPathNavigator Class to Access an External Data Source</span></span>
<span data-ttu-id="d5ad1-158"><a name="InfoPath2007XPathNavigatorClassFormTemplates_SelectingXMLNodes"> </a></span><span class="sxs-lookup"><span data-stu-id="d5ad1-158"></span></span>

<span data-ttu-id="d5ad1-p116">Pour accéder à une source de données externe associée au formulaire, envoyez le nom de la source de données à la propriété [DataSources](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.DataSources.aspx) de la classe [XmlForm](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.aspx) . Pour créer une connexion à une autre source de données externe, ou pour voir la liste des noms des connexions de sources de données existantes, cliquez sur **Connexions de données** dans l'onglet **Données** du Ruban.</span><span class="sxs-lookup"><span data-stu-id="d5ad1-p116">To access an external data source associated with the form, pass the name of the data source to the [DataSources](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.DataSources.aspx) property of the [XmlForm](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.aspx) class. To create a connection to a new external data source, or to view a list of the names of existing external data source connections, click **Data Connections** on the **Data** tab of the ribbon.</span></span> 
  
<span data-ttu-id="d5ad1-p117">L'exemple de code suivant illustre la création d'un objet **XPathNavigator** placé à la racine d'une source de données externe nommée CityList (Liste des villes) à l'aide de la méthode **CreateNavigator**, puis l'utilisation de la propriété **OuterXml** de la classe **XPathNavigator** pour afficher le code XML retourné dans une zone de message.</span><span class="sxs-lookup"><span data-stu-id="d5ad1-p117">The following code sample shows how to create an **XPathNavigator** object positioned at the root of an external data source named "CityList" by using the **CreateNavigator** method, and then uses the **OuterXml** property of the **XPathNavigator** class to display the XML returned in a message box. This code sample assumes that you created a data connection to a list of city names that are stored in an external data source, such as an XML document or a SharePoint list, and named that data connection "CityList."</span></span> 
  
```cs
XPathNavigator myNavigator = 
   this.DataSources["CityList"].CreateNavigator();
MessageBox.Show("External data source XML: " + 
   myNavigator.OuterXml.ToString());
```

```vb
Dim myNavigator As XPathNavigator  = _
   Me.DataSources("CityList").CreateNavigator()
MessageBox.Show("External data source XML: " &amp; _
   myNavigator.OuterXml.ToString())
```

<span data-ttu-id="d5ad1-163">Une fois que vous avez accédé à l'objet **XPathNavigator** placé à la racine de la source de données externe, vous pouvez utiliser les membres de la classe **XPathNavigator** tels que les méthodes **SelectSingleNode** et **SetValue** pour utiliser les données.</span><span class="sxs-lookup"><span data-stu-id="d5ad1-163">After you have access to an **XPathNavigator** object positioned at the root of an external data source, you can use members of the **XPathNavigator** class such as the **SelectSingleNode** and **SetValue** methods to work with the data it contains.</span></span> 
  
## <a name="infopath-object-model-members-that-use-the-xpathnavigator-and-xpathnodeiterator-classes"></a><span data-ttu-id="d5ad1-164">Membres du modèle objet InfoPath qui utilisent les classes XPathNavigator et XPathNodeIterator</span><span class="sxs-lookup"><span data-stu-id="d5ad1-164">InfoPath Object Model Members That Use the XPathNavigator and XPathNodeIterator Classes</span></span>
<span data-ttu-id="d5ad1-165"><a name="InfoPath2007XPathNavigatorClassFormTemplates_SelectingXMLNodes"> </a></span><span class="sxs-lookup"><span data-stu-id="d5ad1-165"></span></span>

<span data-ttu-id="d5ad1-166">Le tableau suivant recense les membres de l'espace de noms **Microsoft.Office.InfoPath** qui utilisent la classe **XPathNavigator** pour accéder aux données XMSL, les manipuler ou les envoyer.</span><span class="sxs-lookup"><span data-stu-id="d5ad1-166">The following table provides a summary of all of the members of the **Microsoft.Office.InfoPath** namespace that use the **XPathNavigator** class to access, manipulate, or submit XML data.</span></span> 
  
|<span data-ttu-id="d5ad1-167">**Classe parent**</span><span class="sxs-lookup"><span data-stu-id="d5ad1-167">**Parent Class**</span></span>|<span data-ttu-id="d5ad1-168">**Membre**</span><span class="sxs-lookup"><span data-stu-id="d5ad1-168">**Member**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="d5ad1-169">AdoQueryConnection</span><span class="sxs-lookup"><span data-stu-id="d5ad1-169">AdoQueryConnection</span></span>](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.AdoQueryConnection.aspx) <br/> |<span data-ttu-id="d5ad1-170">Méthode [BuildSqlFromXmlNodes](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.AdoQueryConnection.BuildSqlFromXmlNodes.aspx)</span><span class="sxs-lookup"><span data-stu-id="d5ad1-170">[BuildSqlFromXmlNodes](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.AdoQueryConnection.BuildSqlFromXmlNodes.aspx) method</span></span>  <br/> |
|[<span data-ttu-id="d5ad1-171">AdoSubmitConnection</span><span class="sxs-lookup"><span data-stu-id="d5ad1-171">AdoSubmitConnection</span></span>](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.AdoSubmitConnection.aspx) <br/> |<span data-ttu-id="d5ad1-172">Méthode [BuildSqlFromXmlNodes](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.AdoSubmitConnection.BuildSqlFromXmlNodes.aspx)</span><span class="sxs-lookup"><span data-stu-id="d5ad1-172">[BuildSqlFromXmlNodes](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.AdoSubmitConnection.BuildSqlFromXmlNodes.aspx) method</span></span>  <br/> |
|[<span data-ttu-id="d5ad1-173">ClickedEventArgs</span><span class="sxs-lookup"><span data-stu-id="d5ad1-173">ClickedEventArgs</span></span>](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ClickedEventArgs.aspx) <br/> |<span data-ttu-id="d5ad1-174">[Source](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ClickedEventArgs.Source.aspx) , propriété</span><span class="sxs-lookup"><span data-stu-id="d5ad1-174">[Source](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ClickedEventArgs.Source.aspx) property</span></span>  <br/> |
|[<span data-ttu-id="d5ad1-175">ContextChangedEventArgs</span><span class="sxs-lookup"><span data-stu-id="d5ad1-175">ContextChangedEventArgs</span></span>](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ContextChangedEventArgs.aspx) <br/> |<span data-ttu-id="d5ad1-176">[Context](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ContextChangedEventArgs.Context.aspx) , propriété</span><span class="sxs-lookup"><span data-stu-id="d5ad1-176">[Context](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ContextChangedEventArgs.Context.aspx) property</span></span>  <br/> |
|[<span data-ttu-id="d5ad1-177">Source de données</span><span class="sxs-lookup"><span data-stu-id="d5ad1-177">DataSource</span></span>](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSource.aspx) <br/> |<span data-ttu-id="d5ad1-178">Méthode [CreateNavigator](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSource.CreateNavigator.aspx)</span><span class="sxs-lookup"><span data-stu-id="d5ad1-178">[CreateNavigator](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSource.CreateNavigator.aspx) method</span></span>  <br/> |
||<span data-ttu-id="d5ad1-179">Méthode [GetNamedNodeProperty](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSource.GetNamedNodeProperty.aspx)</span><span class="sxs-lookup"><span data-stu-id="d5ad1-179">[GetNamedNodeProperty](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSource.GetNamedNodeProperty.aspx) method</span></span>  <br/> |
||<span data-ttu-id="d5ad1-180">Méthode [SetNamedNodeProperty](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSource.SetNamedNodeProperty.aspx)</span><span class="sxs-lookup"><span data-stu-id="d5ad1-180">[SetNamedNodeProperty](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSource.SetNamedNodeProperty.aspx) method</span></span>  <br/> |
|[<span data-ttu-id="d5ad1-181">EmailSubmitConnection</span><span class="sxs-lookup"><span data-stu-id="d5ad1-181">EmailSubmitConnection</span></span>](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.EmailSubmitConnection.aspx) <br/> |<span data-ttu-id="d5ad1-182">Méthode [Execute](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.EmailSubmitConnection.Execute.aspx)</span><span class="sxs-lookup"><span data-stu-id="d5ad1-182">[Execute](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.EmailSubmitConnection.Execute.aspx) method</span></span>  <br/> |
|[<span data-ttu-id="d5ad1-183">FileQueryConnection</span><span class="sxs-lookup"><span data-stu-id="d5ad1-183">FileQueryConnection</span></span>](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FileQueryConnection.aspx) <br/> |<span data-ttu-id="d5ad1-184">Méthode [Execute](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FileQueryConnection.Execute.aspx)</span><span class="sxs-lookup"><span data-stu-id="d5ad1-184">[Execute](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FileQueryConnection.Execute.aspx) method</span></span>  <br/> |
|[<span data-ttu-id="d5ad1-185">FileSubmitConnection</span><span class="sxs-lookup"><span data-stu-id="d5ad1-185">FileSubmitConnection</span></span>](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FileSubmitConnection.aspx) <br/> |<span data-ttu-id="d5ad1-186">Méthode [Execute](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FileSubmitConnection.Execute.aspx)</span><span class="sxs-lookup"><span data-stu-id="d5ad1-186">[Execute](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FileSubmitConnection.Execute.aspx) method</span></span>  <br/> |
|[<span data-ttu-id="d5ad1-187">FormError</span><span class="sxs-lookup"><span data-stu-id="d5ad1-187">FormError</span></span>](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormError.aspx) <br/> |<span data-ttu-id="d5ad1-188">Propriété [site](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormError.Site.aspx)</span><span class="sxs-lookup"><span data-stu-id="d5ad1-188">[Site](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormError.Site.aspx) property</span></span>  <br/> |
|[<span data-ttu-id="d5ad1-189">FormErrorCollection</span><span class="sxs-lookup"><span data-stu-id="d5ad1-189">FormErrorCollection</span></span>](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormErrorCollection.aspx) <br/> |<span data-ttu-id="d5ad1-190">[Ajouter](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormErrorCollection.Add.aspx) des méthodes</span><span class="sxs-lookup"><span data-stu-id="d5ad1-190">[Add](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormErrorCollection.Add.aspx) methods</span></span>  <br/> |
|[<span data-ttu-id="d5ad1-191">Modèle de formulaire</span><span class="sxs-lookup"><span data-stu-id="d5ad1-191">FormTemplate</span></span>](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormTemplate.aspx) <br/> |<span data-ttu-id="d5ad1-192">Propriété [manifeste](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormTemplate.Manifest.aspx)</span><span class="sxs-lookup"><span data-stu-id="d5ad1-192">[Manifest](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormTemplate.Manifest.aspx) property</span></span>  <br/> |
|[<span data-ttu-id="d5ad1-193">MergeEventArgs</span><span class="sxs-lookup"><span data-stu-id="d5ad1-193">MergeEventArgs</span></span>](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.MergeEventArgs.aspx) <br/> |<span data-ttu-id="d5ad1-194">Propriété [XML](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.MergeEventArgs.Xml.aspx)</span><span class="sxs-lookup"><span data-stu-id="d5ad1-194">[Xml](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.MergeEventArgs.Xml.aspx) property</span></span>  <br/> |
|[<span data-ttu-id="d5ad1-195">SharepointListQueryConnection</span><span class="sxs-lookup"><span data-stu-id="d5ad1-195">SharepointListQueryConnection</span></span>](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SharepointListQueryConnection.aspx) <br/> |<span data-ttu-id="d5ad1-196">Méthode [Execute](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SharepointListQueryConnection.Execute.aspx)</span><span class="sxs-lookup"><span data-stu-id="d5ad1-196">[Execute](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SharepointListQueryConnection.Execute.aspx) method</span></span>  <br/> |
|[<span data-ttu-id="d5ad1-197">Signature</span><span class="sxs-lookup"><span data-stu-id="d5ad1-197">Signature</span></span>](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Signature.aspx) <br/> |<span data-ttu-id="d5ad1-198">[SignatureBlockXmlNode,](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Signature.SignatureBlockXmlNode.aspx) propriété</span><span class="sxs-lookup"><span data-stu-id="d5ad1-198">[SignatureBlockXmlNode](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Signature.SignatureBlockXmlNode.aspx) property</span></span>  <br/> |
|[<span data-ttu-id="d5ad1-199">SignedDataBlock</span><span class="sxs-lookup"><span data-stu-id="d5ad1-199">SignedDataBlock</span></span>](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignedDataBlock.aspx) <br/> |<span data-ttu-id="d5ad1-200">[SignatureContainer,](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignedDataBlock.SignatureContainer.aspx) propriété</span><span class="sxs-lookup"><span data-stu-id="d5ad1-200">[SignatureContainer](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignedDataBlock.SignatureContainer.aspx) property</span></span>  <br/> |
|[<span data-ttu-id="d5ad1-201">View</span><span class="sxs-lookup"><span data-stu-id="d5ad1-201">View</span></span>](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.aspx) <br/> |<span data-ttu-id="d5ad1-202">Méthodes [GetContextNodes](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.GetContextNodes.aspx)</span><span class="sxs-lookup"><span data-stu-id="d5ad1-202">[GetContextNodes](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.GetContextNodes.aspx) methods</span></span>  <br/> |
||<span data-ttu-id="d5ad1-203">Méthodes [SelectNodes](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectNodes.aspx)</span><span class="sxs-lookup"><span data-stu-id="d5ad1-203">[SelectNodes](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectNodes.aspx) methods</span></span>  <br/> |
||<span data-ttu-id="d5ad1-204">Méthodes [SelectText](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectText.aspx)</span><span class="sxs-lookup"><span data-stu-id="d5ad1-204">[SelectText](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectText.aspx) methods</span></span>  <br/> |
|[<span data-ttu-id="d5ad1-205">WebServiceConnection</span><span class="sxs-lookup"><span data-stu-id="d5ad1-205">WebServiceConnection</span></span>](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.WebServiceConnection.aspx) <br/> |<span data-ttu-id="d5ad1-206">Méthode [Execute](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.WebServiceConnection.Execute.aspx)</span><span class="sxs-lookup"><span data-stu-id="d5ad1-206">[Execute](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.WebServiceConnection.Execute.aspx) method</span></span>  <br/> |
||<span data-ttu-id="d5ad1-207">Méthode [GenerateDataSetDiffGram](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.WebServiceConnection.GenerateDataSetDiffGram.aspx)</span><span class="sxs-lookup"><span data-stu-id="d5ad1-207">[GenerateDataSetDiffGram](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.WebServiceConnection.GenerateDataSetDiffGram.aspx) method</span></span>  <br/> |
|[<span data-ttu-id="d5ad1-208">XmlEventArgs</span><span class="sxs-lookup"><span data-stu-id="d5ad1-208">XmlEventArgs</span></span>](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlEventArgs.aspx) <br/> |<span data-ttu-id="d5ad1-209">Propriété [OldParent](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlEventArgs.OldParent.aspx)</span><span class="sxs-lookup"><span data-stu-id="d5ad1-209">[OldParent](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlEventArgs.OldParent.aspx) property</span></span>  <br/> |
||<span data-ttu-id="d5ad1-210">Propriété [site](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlEventArgs.Site.aspx)</span><span class="sxs-lookup"><span data-stu-id="d5ad1-210">[Site](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlEventArgs.Site.aspx) property</span></span>  <br/> |
|[<span data-ttu-id="d5ad1-211">XmlForm</span><span class="sxs-lookup"><span data-stu-id="d5ad1-211">XmlForm</span></span>](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.aspx) <br/> |<span data-ttu-id="d5ad1-212">Propriété [MainDataSource](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.MainDataSource.aspx) , qui renvoie un objet **DataSource** qui à son tour fournit la méthode **CreateNavigator** pour la création d’un objet **XPathNavigator** placé à la racine du document XML sous-jacent du formulaire (données principale source).</span><span class="sxs-lookup"><span data-stu-id="d5ad1-212">[MainDataSource](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.MainDataSource.aspx) property, which returns a **DataSource** object that in turn provides the **CreateNavigator** method for creating an **XPathNavigator** object positioned at the root of the form's underlying XML document (main data source).</span></span>  <br/> |
||<span data-ttu-id="d5ad1-213">Méthode [MergeForm](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.MergeForm.aspx)</span><span class="sxs-lookup"><span data-stu-id="d5ad1-213">[MergeForm](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.MergeForm.aspx) method</span></span>  <br/> |
|[<span data-ttu-id="d5ad1-214">XmlFormCollection</span><span class="sxs-lookup"><span data-stu-id="d5ad1-214">XmlFormCollection</span></span>](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlFormCollection.aspx) <br/> |<span data-ttu-id="d5ad1-215">Méthode [NewFromFormTemplate](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlFormCollection.NewFromFormTemplate.aspx)</span><span class="sxs-lookup"><span data-stu-id="d5ad1-215">[NewFromFormTemplate](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlFormCollection.NewFromFormTemplate.aspx) method</span></span>  <br/> |
|[<span data-ttu-id="d5ad1-216">XmlValidatingEventArgs</span><span class="sxs-lookup"><span data-stu-id="d5ad1-216">XmlValidatingEventArgs</span></span>](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlValidatingEventArgs.aspx) <br/> |<span data-ttu-id="d5ad1-217">Méthodes [ReportError](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlValidatingEventArgs.ReportError.aspx)</span><span class="sxs-lookup"><span data-stu-id="d5ad1-217">[ReportError](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlValidatingEventArgs.ReportError.aspx) methods</span></span>  <br/> |
   
<span data-ttu-id="d5ad1-218">Outre les membres du modèle objet InfoPath qui retournent ou acceptent un objet **XPathNavigator**, les méthodes suivantes retournent une instance de la classe **XPathNodeIterator** de l'espace de noms **System.Xml.XPath** pour parcourir les nœuds XML des éléments qui sont spécifiés ou sélectionnés dans un affichage.</span><span class="sxs-lookup"><span data-stu-id="d5ad1-218">In addition to the InfoPath object model members that return or accept an **XPathNavigator** object, the following methods return an instance of the **XPathNodeIterator** class of the **System.Xml.XPath** namespace for iterating over the XML nodes of items that are specified or selected in a view.</span></span> 
  
|<span data-ttu-id="d5ad1-219">**Classe parent**</span><span class="sxs-lookup"><span data-stu-id="d5ad1-219">**Parent Class**</span></span>|<span data-ttu-id="d5ad1-220">**Membre**</span><span class="sxs-lookup"><span data-stu-id="d5ad1-220">**Member**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="d5ad1-221">View</span><span class="sxs-lookup"><span data-stu-id="d5ad1-221">View</span></span>](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.aspx) <br/> |<span data-ttu-id="d5ad1-222">Méthodes [GetContextNodes](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.GetContextNodes.aspx)</span><span class="sxs-lookup"><span data-stu-id="d5ad1-222">[GetContextNodes](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.GetContextNodes.aspx) methods</span></span>  <br/> |
||<span data-ttu-id="d5ad1-223">Méthode [GetSelectedNodes](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.GetSelectedNodes.aspx)</span><span class="sxs-lookup"><span data-stu-id="d5ad1-223">[GetSelectedNodes](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.GetSelectedNodes.aspx) method</span></span>  <br/> |
   
## <a name="using-the-xpathnavigator-and-xpathnodeiterator-classes-to-work-with-data-selected-in-a-view"></a><span data-ttu-id="d5ad1-224">Utilisation des classes XPathNavigator et XPathNodeIterator pour travailler avec des données sélectionnées dans un affichage</span><span class="sxs-lookup"><span data-stu-id="d5ad1-224">Using the XPathNavigator and XPathNodeIterator Classes to Work with Data Selected in a View</span></span>
<span data-ttu-id="d5ad1-225"><a name="InfoPath2007XPathNavigatorClassFormTemplates_SelectingXMLNodes"> </a></span><span class="sxs-lookup"><span data-stu-id="d5ad1-225"></span></span>

<span data-ttu-id="d5ad1-226">L'exemple suivant utilise les membres des classes **XPathNavigator** et **XPathNodeIterator** pour utiliser des données de formulaires dans la séquence suivante :</span><span class="sxs-lookup"><span data-stu-id="d5ad1-226">The following example uses members of both the **XPathNavigator** and **XPathNodeIterator** classes to work with form data in the following sequence:</span></span> 
  
1. <span data-ttu-id="d5ad1-227">La méthode **CreateNavigator** de la classe **DataSource** permet de créer une variable objet **XPathNavigator** appelée Ligne1TableauExtensible, placée par défaut à la racine du document XML sous-jacent du formulaire (source de données principale).</span><span class="sxs-lookup"><span data-stu-id="d5ad1-227">The **CreateNavigator** method of the **DataSource** class is used to create an **XPathNavigator** object variable named repeatingTableRow1, which by default is positioned at the root of the underlying XML document of the form (the main data source).</span></span>
    
2. <span data-ttu-id="d5ad1-228">La méthode **SelectSingleNode** de la classe **XPathNavigator** permet de déplacer l'objet **XPathNavigator** vers la première ligne d'un contrôle **Tableau extensible** rattaché à groupe2 dans la source de données.</span><span class="sxs-lookup"><span data-stu-id="d5ad1-228">The **SelectSingleNode** method of the **XPathNavigator** class is used to move the position of the **XPathNavigator** object to the first row of a **Repeating Table** control bound to group2 in the data source.</span></span> 
    
3. <span data-ttu-id="d5ad1-229">La variable de l'objet Ligne1TableauExtensible est transmise à la méthode **SelectNodes** de la classe **View** pour sélectionner les nœuds de la ligne.</span><span class="sxs-lookup"><span data-stu-id="d5ad1-229">The repeatingTableRow1 object variable is passed to the **SelectNodes** method of the **View** class to select the nodes in that row.</span></span> 
    
4. <span data-ttu-id="d5ad1-230">Une variable objet **XPathNodeIterator** nommée Nœuds sélectionnés est déclarée, et la méthode **GetSelectedNodes** de la classe **View** est utilisée pour compléter l'objet **XPathNodeIterator** avec les nœuds sélectionnés.</span><span class="sxs-lookup"><span data-stu-id="d5ad1-230">An **XPathNodeIterator** object variable named selectedNodes is declared and the **GetSelectedNodes** method of the **View** class is used populate the **XPathNodeIterator** object with the selected nodes.</span></span> 
    
5. <span data-ttu-id="d5ad1-231">La propriété **Count** de la classe **XPathNodeIterator** permet d'afficher le nombre de nœuds contenus dans la variable objet NœudsSélectionnés.</span><span class="sxs-lookup"><span data-stu-id="d5ad1-231">The **Count** property of the **XPathNodeIterator** class is used to display the number of nodes contained in the selectedNodes object variable.</span></span> 
    
6. <span data-ttu-id="d5ad1-232">Une boucle For/Each permet de parcourir les nœuds de la variable objet NœudsSélectionnés et d'afficher des informations sur chaque nœud à l'aide des propriétés **Name**, **InnerXml** et **Value** de la classe **XPathNavigator**.</span><span class="sxs-lookup"><span data-stu-id="d5ad1-232">A For/Each loop is used to iterate over the nodes in the selectedNodes object variable and display information about each node using the **Name**, **InnerXml**, and **Value** properties of the **XPathNavigator** class.</span></span> 
    
```cs
// Create XPathNavigator and specify XPath for nodes.
XPathNavigator repeatingTableRow1 = 
   this.CreateNavigator().SelectSingleNode(
   "/my:myFields/my:group1/my:group2[1]", NamespaceManager);
// Select nodes in specified XPathNavigator.
CurrentView.SelectNodes(repeatingTableRow1);
// Get selected nodes.
XPathNodeIterator selectedNodes = 
   CurrentView.GetSelectedNodes();
// Display the count of selected nodes.
MessageBox.Show(selectedNodes.Count.ToString());
// Loop through collection and display information.
foreach (XPathNavigator selectedNode in selectedNodes)
{
   MessageBox.Show(selectedNode.Name);
   MessageBox.Show(selectedNode.InnerXml);
   MessageBox.Show(selectedNode.Value);
}
```

```vb
' Create XPathNavigator and specify XPath for nodes.
Dim repeatingTableRow1 As XPathNavigator  = _
   Me.CreateNavigator().SelectSingleNode( _
   "/my:myFields/my:group1/my:group2[1]", NamespaceManager)
' Select nodes in specified XPathNavigator.
CurrentView.SelectNodes(repeatingTableRow1)
' Get selected nodes.
Dim selectedNodes As XPathNodeIterator = _
   CurrentView.GetSelectedNodes()
' Display the count of selected nodes.
MessageBox.Show(selectedNodes.Count.ToString())
' Loop through collection and display information.
Dim selectedNode As XPathNavigator
For Each selectedNode In selectedNodes
   MessageBox.Show(selectedNode.Name)
   MessageBox.Show(selectedNode.InnerXml)
   MessageBox.Show(selectedNode.Value)
Next
```

<span data-ttu-id="d5ad1-233">Pour plus d’informations sur l’utilisation des données XML à partir de modèles de formulaire InfoPath, voir Utilisation des données XML à l’aide la classe XPathNavigator dans les modèles de formulaire InfoPath 2007.</span><span class="sxs-lookup"><span data-stu-id="d5ad1-233">For more information about how to work with XML data from InfoPath form templates, see Working with XML Data Using the XPathNavigator Class in InfoPath 2007 Form Templates.</span></span>
  

