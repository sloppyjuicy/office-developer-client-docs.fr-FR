---
title: Travailler avec les classes XPathNavigator et XPathNodeIterator
manager: soliver
ms.date: 12/07/2015
ms.audience: Developer
keywords:
- xpathnodeiterator class [infopath 2007],XPathNavigator class [InfoPath 2007],form XML data [InfoPath 2007], accessing,XML DOM [InfoPath 2007],converting MSXML5 script [InfoPath 2007],MSXML5 script [InfoPath 2007], converting
ms.localizationpriority: medium
ms.assetid: 72fb3ee5-f18e-4f9c-adc6-698ac037b79d
description: Pour accéder aux données XML dans les sources de données du modèle de formulaire et les manipuler, un grand nombre de membres du modèle objet avec code managé fourni par l'espace de noms Microsoft.Office.InfoPath créent ou se voient attribuer une instance de la classe XPathNavigator de l'espace de noms System.Xml.XPath. Après avoir accédé à un objet XPathNavigator retourné par un membre du modèle objet InfoPath, vous pouvez utiliser les propriétés et les méthodes de la classe XPathNavigator pour travailler avec les données.
ms.openlocfilehash: e8d28629eb00d1731c214941f3bf07c89e54e781
ms.sourcegitcommit: 518845d053a009b11c8d907a33822161c0b6bc96
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/08/2022
ms.locfileid: "63380577"
---
# <a name="work-with-the-xpathnavigator-and-xpathnodeiterator-classes"></a>Travailler avec les classes XPathNavigator et XPathNodeIterator

Pour accéder aux données XML dans les sources de données du modèle de formulaire et les manipuler, un grand nombre de membres du modèle objet avec code managé fourni par l'espace de noms [Microsoft.Office.InfoPath](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.aspx) créent ou se voient attribuer une instance de la classe **XPathNavigator** de l'espace de noms **System.Xml.XPath**. Après avoir accédé à un objet **XPathNavigator** retourné par un membre du modèle objet InfoPath, vous pouvez utiliser les propriétés et les méthodes de la classe **XPathNavigator** pour travailler avec les données.
  
Le membre le plus couramment utilisé de l'espace de noms **Microsoft.Office.InfoPath** qui utilise la classe **XPathNavigator** est la méthode [CreateNavigator](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSource.CreateNavigator.aspx) de la classe [DataSource](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSource.aspx) qui vous permet d'utiliser les données stockées représentées par un objet **DataSource**. La méthode **CreateNavigator** crée un objet **XPathNavigator** placé à la racine de la source de données représentée par l'objet **DataSource**.
  
> [!TIP]
> [!CONSEIL] Si vous avez l'habitude d'utiliser MSXML5 à partir du script pour travailler avec des données dans Microsoft InfoPath 2003, vous pouvez considérer la méthode **CreateNavigator** en remplacement de la propriété **DOM** de l'objet **DataObject**.
  
## <a name="using-the-xpathnavigator-class-to-access-the-main-data-source-of-the-form"></a>Utilisation de la classe XPathNavigator pour accéder à la source principale de données du formulaire

Pour accéder à la source de données principale du formulaire, appelez la méthode [CreateNavigator](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSource.CreateNavigator.aspx) directement depuis le mot clé **this** (C#) ou **Me** (Visual Basic). L'exemple suivant crée un objet **XPathNavigator** placé à la racine de la source de données principale à l'aide de la méthode **CreateNavigator**, puis utilise la propriété **OuterXml** de la classe **XPathNavigator** pour afficher le code XML retourné dans une zone de message.
  
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
> [!REMARQUE] L'appel à la méthode [CreateNavigator](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSource.CreateNavigator.aspx) directement depuis le mot clé **this** ou **Me** équivaut à appeler la méthode [CreateNavigator](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSource.CreateNavigator.aspx) à l'aide de la propriété [MainDataSource](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.MainDataSource.aspx) (  `this.MainDataSource.CreateNavigator()`) ou à passer une chaîne vide à la propriété [DataSources](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.DataSources.aspx) de la classe [XmlForm](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.aspx) (  `this.DataSources[""].CreateNavigator()`).
  
## <a name="selecting-and-setting-the-xml-nodes-for-fields-in-the-main-data-source"></a>Sélection et définition de nœuds XML pour les champs de la source de données principale

<a name="InfoPath2007XPathNavigatorClassFormTemplates_SelectingXMLNodes"> </a>

Pour sélectionner un nœud XML unique pour champ de la source de données, utilisez la méthode **SelectSingleNode(String,IXmlNamespaceResolver)** de la classe **XPathNavigator**. Si vous voulez utiliser un jeu de champs récurrents ou de groupes récurrents, utilisez la méthode **Select(String,IXmlNamespaceResolver)** de la classe **XPathNavigator**. Cette méthode retourne un objet **XPathNodeIterator** qui représente une collection de nœuds.
  
### <a name="selecting-and-setting-the-value-of-a-single-node"></a>Sélection et définition de la valeur d’un nœud unique

La méthode **SelectSingleNode** surchargée que vous devez utiliser possède un paramètre _xpath_ qui prend une expression XPath sous forme de chaîne et un  paramètre de résolution qui prend un objet **XmlNamespaceManager** pour résoudre les préfixes d’espace de noms. Pour sélectionner un nœud unique dans la source de données principale du formulaire, passez une expression XPath qui spécifie le champ ou le groupe à sélectionner pour le paramètre _xpath_ , ainsi que l’objet **XmlNamespaceManager** renvoyé par la propriété [NamespaceManager](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.NamespaceManager.aspx) de l’objet **XmlForm** . L'objet **XmlNamespaceManager** retourné est initialisé lors du chargement avec tous les espaces de noms définis par le fichier de définition de formulaire du modèle de formulaire (.xsf).
  
> [!TIP]
> [!CONSEIL] La façon la plus simple de créer une expression XPath pour sélectionner un nœud dans la source de données du formulaire est de cliquer avec le bouton droit sur le champ ou sur le groupe dans le volet Office **Champs**, puis de cliquer sur **Copier XPath**. Pour créer et tester des expressions XPath modifiées manuellement pour accéder à des nœuds dans un schéma XML complexe ou fortement imbriqué, ajoutez un contrôle **Zone d'expression** au formulaire, spécifiez l'expression XPath du contrôle, puis affichez l'aperçu du formulaire pour afficher les résultats.
  
L'exemple qui suit utilise la méthode **SelectSingleNode** pour sélectionner le nœud unique du champ  `EmailAlias`. Il utilise ensuite la méthode **SetValue** de la classe **XPathNavigator** et la propriété [UserName](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.User.UserName.aspx) de la classe [User](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.User.aspx) pour définir la valeur du champ sur celle de l'alias de l'utilisateur actuel.
  
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

Pour plus d'informations sur la création d'expressions XPath, voir XPath Reference (éventuellement en anglais) sur MSDN, ainsi que les [recommandations du W3C sur le langage XML Path (XPath) Version 1.0 (éventuellement en anglais)](https://www.w3.org/TR/xpath).
  
### <a name="setting-the-value-of-a-node-that-has-the-xsinil-attribute"></a>Définition de la valeur d’un nœud qui possède l’attribut xsi:nil

Pour certains types de données, le fait de définir une valeur nulle par programme génère l'erreur « La validation de schéma a détecté des erreurs qui ne concernent pas le type de données ». En général, la cause de cette erreur est que l'attribut [xsi:nil (éventuellement en anglais)](https://www.w3.org/TR/2001/REC-xmlschema-1-20010502/#xsi_nil) de l'élément est défini sur **true**. Si vous examinez l'élément XML sous-jacent du champ vierge du formulaire, vous verrez ce paramètre. Par exemple, l'attribut **xsi:nil** du fragment XML du champ Date vierge suivant est défini sur **true**.
  
```XML
<my:myDate xsi:nil="true"></my:myDate>
```

Si l'attribut **xsi:nil** est défini sur **true**, il indique que l'élément est présent mais n'a pas de valeur, en d'autres termes est null. Si vous essayez de définir la valeur d'un tel nœud par programme, InfoPath affiche l'erreur « La validation de schéma a détecté des erreurs qui ne concernent pas le type de données. », car l'élément est signalé comme null. InfoPath définit l'attribut **xsi:nil** sur **true** pour les champs null des types de données suivants :
  
- **Whole Number (integer)**

- **Decimal (double)**

- **Date (date)**

- **Time (time)**

- **Date and Time (dateTime)**

Pour empêcher cette erreur, votre code doit rechercher la présence de l'attribut **xsi:nil**. S'il est présent, supprimez-le avant de définir la valeur du nœud. La sous-routine qui suit prend un objet **XpathNavigator** placé sur le nœud que vous souhaitez définir, recherche l'attribut **nil** et le supprime s'il existe.
  
```cs
public void DeleteNil(XPathNavigator node)
{
   if (node.MoveToAttribute(
      "nil", "https://www.w3.org/2001/XMLSchema-instance"))
      node.DeleteSelf();
}
```

```vb
Public Sub DeleteNil(ByVal node As XPathNavigator)
   If (node.MoveToAttribute( _
      "nil", "https://www.w3.org/2001/XMLSchema-instance")) Then
      node.DeleteSelf()
   End If
End Sub
```

Vous pouvez appeler cette sous-routine avant d'essayer de définir un champ d'un type de données qui peut avoir l'attribut **xsi:nil**, comme présenté dans l'exemple ci-dessous, qui définit un champ Date.
  
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
> [!REMARQUE] Bien que l'implémentation de l'objet **XPathNavigator** dans InfoPath expose la méthode **SetTypedValue**, qui est utilisée pour définir un nœud à l'aide d'une valeur de type spécifique, InforPath n'utilise pas cette méthode. Vous devez utiliser la méthode **SetValue**, et transmettre une valeur de chaîne au format correct pour le type de données du nœud.
  
### <a name="selecting-and-setting-a-set-of-repeating-nodes"></a>Sélection et définition d’un jeu de nœuds récurrents

Pour spécifier des champs ou des groupes récurrents dont le nombre n'est pas déterminé, utilisez la méthode **Select** de la classe **XPathNavigator**. Cette méthode retourne un objet XPathNodeIterator que vous pouvez utiliser pour parcourir la collection de nœuds.
  
Dans l'exemple suivant, votre modèle de formulaire contient une **Liste à puces** ou un autre contrôle récurrent qui est lié à un élément récurrent appelé  `field1`. Le XPath de ce champ est transmis à la méthode **Select** et la valeur **XPathNodeIterator** retournée est affectée à la variable  `nodes`. Vous pouvez utiliser la méthode MoveNext pour parcourir la collection de nœuds et la propriété Current pour retourner un objet **XPathNavigator** placé sur le nœud actif. Enfin, utilisez la **propriété Value** pour extraire et afficher la valeur de chaque champ ext. exex.
  
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

L'exemple qui précède fonctionne avec des valeurs de chaîne dans le champ récurrent spécifié. Cependant, si ce champ contient des valeurs numériques, vous pouvez utiliser un code similaire pour parcourir les valeurs du champ et effectuer des opération, par exemple le calcul du total ou de la moyenne des valeurs.
  
De même, plutôt que d'utiliser la propriété **Value** pour récupérer la valeur de chaque instance du champ récurrent, vous pouvez utiliser la méthode **SetValue** pour parcourir les champs et en définir les valeurs, comme illustré dans l'exemple qui suit.
  
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

## <a name="using-the-xpathnavigator-class-to-access-an-external-data-source"></a>Utilisation de la classe XPathNavigator pour accéder à une source de données externe

<a name="InfoPath2007XPathNavigatorClassFormTemplates_SelectingXMLNodes"> </a>

Pour accéder à une source de données externe associée au formulaire, envoyez le nom de la source de données à la propriété [DataSources](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.DataSources.aspx) de la classe [XmlForm](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.aspx) . Pour créer une connexion à une autre source de données externe, ou pour voir la liste des noms des connexions de sources de données existantes, cliquez sur **Connexions de données** dans l'onglet **Données** du Ruban.
  
L'exemple de code suivant illustre la création d'un objet **XPathNavigator** placé à la racine d'une source de données externe nommée CityList (Liste des villes) à l'aide de la méthode **CreateNavigator**, puis l'utilisation de la propriété **OuterXml** de la classe **XPathNavigator** pour afficher le code XML retourné dans une zone de message.
  
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

Une fois que vous avez accédé à l'objet **XPathNavigator** placé à la racine de la source de données externe, vous pouvez utiliser les membres de la classe **XPathNavigator** tels que les méthodes **SelectSingleNode** et **SetValue** pour utiliser les données.
  
## <a name="infopath-object-model-members-that-use-the-xpathnavigator-and-xpathnodeiterator-classes"></a>Membres du modèle objet InfoPath qui utilisent les classes XPathNavigator et XPathNodeIterator

<a name="InfoPath2007XPathNavigatorClassFormTemplates_SelectingXMLNodes"> </a>

Le tableau suivant recense les membres de l'espace de noms **Microsoft.Office.InfoPath** qui utilisent la classe **XPathNavigator** pour accéder aux données XMSL, les manipuler ou les envoyer.
  
|**Classe parent**|**Membre**|
|:-----|:-----|
|[AdoQueryConnection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.AdoQueryConnection.aspx) <br/> |[Méthode BuildSqlFromXmlNodes](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.AdoQueryConnection.BuildSqlFromXmlNodes.aspx)  <br/> |
|[AdoSubmitConnection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.AdoSubmitConnection.aspx) <br/> |[Méthode BuildSqlFromXmlNodes](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.AdoSubmitConnection.BuildSqlFromXmlNodes.aspx)  <br/> |
|[ClickedEventArgs](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ClickedEventArgs.aspx) <br/> |[Source,](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ClickedEventArgs.Source.aspx) propriété  <br/> |
|[ContextChangedEventArgs](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ContextChangedEventArgs.aspx) <br/> |[Propriété Context](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ContextChangedEventArgs.Context.aspx)  <br/> |
|[DataSource](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSource.aspx) <br/> |[CreateNavigator,](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSource.CreateNavigator.aspx) méthode  <br/> |
||[Méthode GetNamedNodeProperty](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSource.GetNamedNodeProperty.aspx)  <br/> |
||[Méthode SetNamedNodeProperty](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSource.SetNamedNodeProperty.aspx)  <br/> |
|[EmailSubmitConnection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.EmailSubmitConnection.aspx) <br/> |[Execute,](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.EmailSubmitConnection.Execute.aspx) méthode  <br/> |
|[FileQueryConnection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FileQueryConnection.aspx) <br/> |[Execute,](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FileQueryConnection.Execute.aspx) méthode  <br/> |
|[FileSubmitConnection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FileSubmitConnection.aspx) <br/> |[Execute,](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FileSubmitConnection.Execute.aspx) méthode  <br/> |
|[FormError](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormError.aspx) <br/> |[Propriété de](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormError.Site.aspx) site  <br/> |
|[FormErrorCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormErrorCollection.aspx) <br/> |[Ajouter](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormErrorCollection.Add.aspx) des méthodes  <br/> |
|[FormTemplate](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormTemplate.aspx) <br/> |[Propriété manifest](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormTemplate.Manifest.aspx)  <br/> |
|[MergeEventArgs](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.MergeEventArgs.aspx) <br/> |[Xml](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.MergeEventArgs.Xml.aspx) , propriété  <br/> |
|[SharepointListQueryConnection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SharepointListQueryConnection.aspx) <br/> |[Execute,](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SharepointListQueryConnection.Execute.aspx) méthode  <br/> |
|[Signature](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Signature.aspx) <br/> |[SignatureBlockXmlNode,](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Signature.SignatureBlockXmlNode.aspx) propriété  <br/> |
|[SignedDataBlock](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignedDataBlock.aspx) <br/> |[SignatureContainer,](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignedDataBlock.SignatureContainer.aspx) propriété  <br/> |
|[View](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.aspx) <br/> |[Méthodes GetContextNodes](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.GetContextNodes.aspx)  <br/> |
||[Méthodes SelectNodes](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectNodes.aspx)  <br/> |
||[Méthodes SelectText](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectText.aspx)  <br/> |
|[WebServiceConnection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.WebServiceConnection.aspx) <br/> |[Execute,](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.WebServiceConnection.Execute.aspx) méthode  <br/> |
||[Méthode GenerateDataSetDiffGram](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.WebServiceConnection.GenerateDataSetDiffGram.aspx)  <br/> |
|[XmlEventArgs](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlEventArgs.aspx) <br/> |[OldParent,](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlEventArgs.OldParent.aspx) propriété  <br/> |
||[Propriété de](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlEventArgs.Site.aspx) site  <br/> |
|[XmlForm](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.aspx) <br/> |[Propriété MainDataSource](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.MainDataSource.aspx) , qui renvoie un objet **DataSource** qui fournit à son tour la méthode **CreateNavigator** pour la création d’un objet **XPathNavigator** positionné à la racine du document XML sous-jacent du formulaire (source de données principale). |
||[MergeForm,](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.MergeForm.aspx) méthode  <br/> |
|[XmlFormCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlFormCollection.aspx) <br/> |[Méthode NewFromFormTemplate](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlFormCollection.NewFromFormTemplate.aspx)  <br/> |
|[XmlValidatingEventArgs](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlValidatingEventArgs.aspx) <br/> |[Méthodes ReportError](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlValidatingEventArgs.ReportError.aspx)  <br/> |

Outre les membres du modèle objet InfoPath qui retournent ou acceptent un objet **XPathNavigator**, les méthodes suivantes retournent une instance de la classe **XPathNodeIterator** de l'espace de noms **System.Xml.XPath** pour parcourir les nœuds XML des éléments qui sont spécifiés ou sélectionnés dans un affichage.
  
|**Classe parent**|**Membre**|
|:-----|:-----|
|[View](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.aspx) <br/> |[Méthodes GetContextNodes](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.GetContextNodes.aspx)  <br/> |
||[Méthode GetSelectedNodes](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.GetSelectedNodes.aspx)  <br/> |

## <a name="using-the-xpathnavigator-and-xpathnodeiterator-classes-to-work-with-data-selected-in-a-view"></a>Utilisation des classes XPathNavigator et XPathNodeIterator pour travailler avec des données sélectionnées dans un affichage

<a name="InfoPath2007XPathNavigatorClassFormTemplates_SelectingXMLNodes"> </a>

L'exemple suivant utilise les membres des classes **XPathNavigator** et **XPathNodeIterator** pour utiliser des données de formulaires dans la séquence suivante :
  
1. La méthode **CreateNavigator** de la classe **DataSource** permet de créer une variable objet **XPathNavigator** appelée Ligne1TableauExtensible, placée par défaut à la racine du document XML sous-jacent du formulaire (source de données principale).

2. La méthode **SelectSingleNode** de la classe **XPathNavigator** permet de déplacer l'objet **XPathNavigator** vers la première ligne d'un contrôle **Tableau extensible** rattaché à groupe2 dans la source de données.

3. La variable de l'objet Ligne1TableauExtensible est transmise à la méthode **SelectNodes** de la classe **View** pour sélectionner les nœuds de la ligne.

4. Une variable objet **XPathNodeIterator** nommée Nœuds sélectionnés est déclarée, et la méthode **GetSelectedNodes** de la classe **View** est utilisée pour compléter l'objet **XPathNodeIterator** avec les nœuds sélectionnés.

5. La propriété **Count** de la classe **XPathNodeIterator** permet d'afficher le nombre de nœuds contenus dans la variable objet NœudsSélectionnés.

6. Une boucle For/Each permet de parcourir les nœuds de la variable objet NœudsSélectionnés et d'afficher des informations sur chaque nœud à l'aide des propriétés **Name**, **InnerXml** et **Value** de la classe **XPathNavigator**.

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

Pour plus d'informations sur l'utilisation de données XML à partir de modèles de formulaire InfoPath, voir Utilisation de données XML à l'aide la classe XPathNavigator dans les modèles de formulaire InfoPath 2007 (éventuellement en anglais).
  