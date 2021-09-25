---
title: Activation de la fusion personnalisée de formulaires InfoPath
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
ms.assetid: f08f9212-af10-1287-477d-adde7674f523
description: The Merge Forms feature of the Microsoft InfoPath editor is designed to combine the data from multiple forms into a single form.
ms.openlocfilehash: 59a1f8a07252c9ae21e165c1377e69122a3953f4
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59580579"
---
# <a name="enable-custom-merging-of-infopath-forms"></a>Activation de la fusion personnalisée de formulaires InfoPath

The **Merge Forms** feature of the Microsoft InfoPath editor is designed to combine the data from multiple forms into a single form. This is also known as data aggregation. If merging forms is enabled, you can click the **File** tab, click **Save &amp; Send**, click **Merge Forms** under **Import &amp; Link**, and then click the **Merge Forms** button to select one or more forms to merge with the currently opened form. The form that is currently open is the target form and the forms selected in the **Merge Forms** dialog box are known as the source forms.
  
L'agrégation des données qui résulte de la fusion de formulaires peut inclure toutes les données contenues dans les formulaires source et cible, ou seulement une partie de ces données. Les opérations par défaut sont les suivantes.
  
- Pour les éléments répétés, les données sont insérées dans l'emplacement correspondant sur le document cible. Cela se produit lorsque l'attribut **MaxOccurs** de l'élément de destination est supérieur à 1. 
    
- Pour les éléments non répétés (c'est-à-dire ceux où **MaxOccurs** est égal à 1), les attributs des éléments source sont ajoutés aux attributs existants de l'élément de destination. 
    
## <a name="creating-a-custom-transform"></a>Création d’une transformation personnalisée

L'opération de fusion par défaut des formulaires fonctionne bien pour les formulaires basés sur le même schéma XML. Dans certains cas, cependant, vous souhaiterez fusionner des formulaires basés sur des schémas différents ou remplacer l'opération de fusion par défaut pour des formulaires qui sont basés sur le même schéma. Pour ces scénarios, vous pouvez créer une transformation XSL qui contient des instructions d'agrégation pour l'opération de fusion. La transformation est appliquée au moment de la fusion pour créer un document DOM qui contient les informations à importer, avec des annotations qui spécifient la façon d'incorporer ces informations dans le document cible. Ces annotations sont des attributs XML dans l'espace de noms  `http://schemas.microsoft.com/office/InfoPath/2003/aggregation`.
  
Les attributs XML et leurs valeurs servent d'instructions d'agrégation sur la façon dont chaque nœud est fusionné dans le document XML de destination. Ces attributs sont décrits dans les sections suivantes.
  
### <a name="select"></a>select

L'attribut **agg:select** contient une expression de chemin absolu XPath qui identifie l'élément de destination. 
  
### <a name="insert"></a>insert

La valeur « insert » pour l'attribut **agg:action** indique à InfoPath d'insérer l'élément source comme enfant de l'élément de destination qui est spécifié par l'attribut **agg:select**. Les enfants de l'élément source sont inclus dans l'opération d'insertion. L'attribut **selectChild** vous permet de sélectionner un certain emplacement pour l'opération d'insertion de nœud. L'attribut **order** permet de spécifier si les éléments source sont insérés avant les éléments de destination existants ou après. La valeur par défaut si l'attribut **order** est absent est « after » (après). 
  
```XML
<my:field1 agg:select="/my:myFields/my:field1"
 agg:action="insert" agg:order="before">Some Value</my:field1>

```

### <a name="replace"></a>replace

La valeur « replace » pour l'attribut **agg:action** indique à InfoPath de remplacer chacun des éléments de destination que l'attribut **select** référence par l'élément source. 
  
```XML
<my:field1 agg:select="/my:myFields/my:field1"
 agg:action="replace">Some Value</my:field1>
```

### <a name="mergeattributes"></a>mergeAttributes

Si la valeur de l'attribut **agg:action** est « mergeAttributes », les attributs de l'élément source sont fusionnés avec les attributs de chacun des éléments de destination référencés par l'attribut **select**. 
  
```XML
<my:PMAwS agg:action="mergeAttributes"
 agg:select="/my:Root/my:PMAwS">
```

### <a name="delete"></a>delete

Si la valeur de l'attribut **agg:action** est « delete », chacun des éléments de destination référencés par l'attribut **select** sont supprimés du document de destination. 
  
```XML
<my:field1 agg:select="/my:myFields/my:field1"
 agg:action="delete"/>
```

En conjonction avec les attributs spécifiés dans l'espace de noms  `http://schemas.microsoft.com/office/InfoPath/2003/aggregation`, vous utilisez l'espace de noms  `http://schemas.microsoft.com/office/infopath/2003/aggregation-target` pour indiquer un objet XSL qui implémente l'interface **IXMLDOMDocument**. La méthode **get-documentElement** est l'un des membres les plus utiles de cette interface.
  
### <a name="get-documentelement"></a>get-documentElement

La fonction **target:get-documentElement** fournit l'accès au DOM (Document Object Model) du document de destination. Vous pouvez l'utiliser pour changer le fonctionnement de l'opération de fusion basé sur le contenu du document de destination. 
  
```XML
<xsl:when test="function-available('target:get-documentElement')">
    <xsl:variable name="target" select="target:get-documentElement()" />
    <xsl:if test="not(boolean($target/my:Customer[Name="MyName"]))">
        <my:Customer agg:action="insert" agg:select="/my:MergeForms" />
    </xsl:if>
</xsl:when>

```

## <a name="steps-for-creating-a-custom-merge"></a>Procédure de création d’une fusion personnalisée

1. Sélectionnez les types de documents XML source à partir desquels fusionner les données. Collectez un échantillon représentatif de chaque type de document source.
    
2. Dérivez le schéma XML de chaque type de document source XML pour un formulaire InfoPath existant. Cette étape s'effectue aisément en exportant le schéma XML avec la commande **Exporter les fichiers source** de l'onglet **Publier** de Backstage. Pour les documents XML qui n'ont pas été créés dans InfoPath, vous pouvez utiliser un outil comme Microsoft Visual Studio pour créer un schéma à partir du document XML échantillon, ou créer un formulaire échantillon à partir du document XML dans InfoPath, puis exporter le schéma que InfoPath dérive de la structure du document. 
    
3. Identifiez les données que vous voulez fusionner à partir de chaque type de document XML source. Cette étape dépend presque entièrement des exigences de vos formulaires source et destination. Pour certains formulaires, vous souhaiterez copier toutes les données du formulaire source. Pour d'autres, vous souhaiterez seulement un ou deux éléments du document XML sous-jacent au formulaire. Lors de l'identification des données à fusionner, soyez très attentif quant aux documents source et de destination pour assurer la correspondance logique des éléments entre les deux formulaires.
    
4. Créez une transformation XSL pour chaque type de document XML source. Cette étape de configuration de la fusion des formulaires est la plus longue. Le but de la transformation XSL est de transformer le document XML source dans un format qui puisse être fusionné dans le formulaire de destination. Lors de la conception de votre transformation, choisissez si vous utilisez la fusion à partir des chemins d'accès aux fichiers XML ou la fusion à partir des instructions d'agrégation InfoPath.
    
    Visual Studio est un outil pratique pour créer des transformations XSL. Visual Studio fournit la coloration de la syntaxe et un plan du document. Il propose automatiquement les balises fermantes pour vos éléments XSL, ce qui contribue à réduire les saisies redondantes et les fautes de frappe difficiles à repérer. Vous pouvez également créer des transformations XSL à l'aide d'un éditeur de texte tel que Notepad.
    
    Commencez par la transformation d'identité, qui est une simple transformation XSL qui produit en sortie le même fichier XML qu'en entrée :
    
    ```XML
        <?xml version="1.0"?> 
        <xsl:stylesheet version="1.0" xmlns:xsl="https://www.w3.org/1999/XSL/Transform" 
        xmlns:agg="http://schemas.microsoft.com/office/infopath/2003/aggregation" 
        xmlns:target="http://schemas.microsoft.com/office/infopath/2003/aggregation-target" 
        xmlns:my="http://schemas.microsoft.com/office/infopath/2003/myXSD/2003-05-29T20:30:47"> 
            <xsl:template match="/"> 
                <xsl:copy> 
                <xsl:apply-templates select="@* | node()" /> 
                </xsl:copy> 
            </xsl:template> 
            <xsl:template match="@* | node()"> 
                <xsl:copy> 
                <xsl:apply-templates select="@* | node()" /> 
                </xsl:copy> 
            </xsl:template> 
        </xsl:stylesheet>
    ```

    Ajoutez ensuite des sections de remplacement pour les éléments auxquels vous souhaitez ajouter un traitement spécial. Par exemple, ce modèle remplace un élément  `<src:Task>` par un élément  `<my:field1>` et affecte la valeur « replace » à l'attribut **agg:action**. 
    
    ```XML
        <xsl:template match="src:Task"> 
            <my:field1 agg:select="/my:myFields/my:field1" agg:action="replace"> 
                <xsl:value-of select="."/> 
            </my:field1> 
        </xsl:template>
    ```

5. Ajoutez les fichiers de transformation XSL et les fichiers de schéma dans le modèle de formulaire. Après avoir dérivé les schémas de chaque type de document source et créé une transformation XSL pour convertir chaque type de document afin que InfoPath puisse fusionner ses données, ajoutez-les en tant que ressources à votre formulaire. Cliquez sur **Fichiers de ressources** sur l'onglet **Données**, puis cliquez sur **Ajouter** dans la boîte de dialogue **Fichiers de ressources**, accédez à votre fichier de schéma ou de transformation XSL, puis cliquez sur **OK**. Effectuez cette opération pour chaque fichier de schéma et de transformation XSL que vous avez créé.
    
    Si les schémas que vous ajoutez utilisent l'attribut **targetNamespace**, vous de devez ajouter un élément propriété au fichier .xsf du formulaire afin que InfoPath connaisse l'espace de noms du schéma. Pour accéder à ce fichier, cliquez sur l'onglet **Fichier**, cliquez sur **Publier**, puis cliquez sur **Exporter les fichiers source**. Sélectionnez un emplacement pour les fichiers, puis cliquez sur **OK**. Enfin, fermez le modèle de formulaire InfoPath en cours de conception.
    
    Accédez à l'emplacement que vous avez spécifié pour les fichiers extraits et recherchez le fichier portant l'extension de nom .xsf. Généralement, ce fichier s'appelle manifest.xsf. Ouvrez-le dans Notepad, recherchez la balise  `<xsf:file>` qui correspond à votre schéma, et ajoutez un élément propriété « namespace » pour spécifier l'espace de noms cible **targetNamespace** comme illustré dans l'exemple suivant. 
    
    ```xml
        <xsf:file name="IndvTasks.xsd"> 
            <xsf:fileProperties> 
                <xsf:property name="fileType" type="string" value="Resource" /> 
                <xsf:property name="namespace" type="string" 
                value="urn:office-microsoft-com:InfoPath-designer-aggregation-IndStatusReport" /> 
            </xsf:fileProperties> 
        </xsf:file>
    ```

6. La dernière étape de préparation de votre formulaire pour prendre en charge la fusion personnalisée consiste à mettre à jour l’élément **importParameters** dans le fichier .xsf associé au formulaire. 

    Tout d’abord,  `<xsf:importParameters>` recherchez la balise dans le fichier .xsf. Pour chaque paire de transformations schéma/XSL que vous avez créée pour votre formulaire, ajoutez un élément **xsf:importSource** à l’élément **xsf:importParameters**  `<xsf:importParameters enabled="yes"> <xsf:importSource name="" schema="IndvTasks.xsd" transform="ImportTasks.xsl"></xsf:importSource> </xsf:importParameters>` : 
    
    **L’attribut** name de l’élément **xsf:importSource** contient le nom du modèle de formulaire qui peut se trouver dans un document XML source. En règle générale, vous pouvez laisser ce vide. **L’attribut de** schéma contient le nom d’un fichier de schéma que vous avez ajouté au modèle de formulaire à l’étape précédente. Enfin, **l’attribut de** transformation contient le nom de la transformation XSL que vous souhaitez utiliser pour convertir des formulaires conformes au schéma. 
    
    Vous pouvez utiliser une transformation personnalisée avec [l’événement Merge](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Merge.aspx) ou par lui-même. 
    
## <a name="creating-a-custom-merge-in-code"></a>Création d’une fusion personnalisée dans le code

La fusion personnalisée avec code est prise en charge par le gestionnaire d'événements [Merge](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Merge.aspx) , avec son attribut **useScriptHandler** correspondant dans l'élément **importParameters** du fichier .xsf associé au formulaire. 

Dans le code managé, vous pouvez activer l'événement [Merge](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Merge.aspx) en activant la case à cocher **Fusionner à l'aide d'un code personnalisé**, puis en cliquant sur le bouton **Modifier**, dans la catégorie **Avancé** de la boîte de dialogue **Options de formulaire** disponible à partir de Backstage. 
  

