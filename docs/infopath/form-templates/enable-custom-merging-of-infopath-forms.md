---
title: Activation de la fusion personnalisée de formulaires InfoPath
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: f08f9212-af10-1287-477d-adde7674f523
description: La fonctionnalité de fusion de formulaires de l’éditeur de Microsoft InfoPath est conçue pour combiner les données de plusieurs formulaires dans un formulaire.
ms.openlocfilehash: e0e6bfc074829f262d7eef3cf7bf6a86c3b2253b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19782351"
---
# <a name="enable-custom-merging-of-infopath-forms"></a><span data-ttu-id="0fed8-103">Activation de la fusion personnalisée de formulaires InfoPath</span><span class="sxs-lookup"><span data-stu-id="0fed8-103">Enable Custom Merging of InfoPath Forms</span></span>

<span data-ttu-id="0fed8-104">La fonctionnalité de **Fusion de formulaires** de l’éditeur de Microsoft InfoPath est conçue pour combiner les données de plusieurs formulaires dans un formulaire.</span><span class="sxs-lookup"><span data-stu-id="0fed8-104">The **Merge Forms** feature of the Microsoft InfoPath editor is designed to combine the data from multiple forms into a single form.</span></span> <span data-ttu-id="0fed8-105">Il est également appelé agrégation de données.</span><span class="sxs-lookup"><span data-stu-id="0fed8-105">This is also known as data aggregation.</span></span> <span data-ttu-id="0fed8-106">Si la fusion de formulaires est activée, vous pouvez cliquez sur l’onglet **fichier** , cliquez sur **Enregistrer &amp; envoyer**, cliquez sur **Fusionner les formulaires** sous **importation &amp; lien**, puis cliquez sur le bouton de **La fusion de formulaires** pour sélectionner un ou plusieurs formulaires à fusionner avec la formulaire actuellement ouvert.</span><span class="sxs-lookup"><span data-stu-id="0fed8-106">If merging forms is enabled, you can click the **File** tab, click **Save &amp; Send**, click **Merge Forms** under **Import &amp; Link**, and then click the **Merge Forms** button to select one or more forms to merge with the currently opened form.</span></span> <span data-ttu-id="0fed8-107">Le formulaire actuellement ouvert est le formulaire cible et les formulaires sélectionnés dans la boîte de dialogue **Fusionner les formulaires** sont appelés des formulaires sources.</span><span class="sxs-lookup"><span data-stu-id="0fed8-107">The form that is currently open is the target form and the forms selected in the **Merge Forms** dialog box are known as the source forms.</span></span>
  
<span data-ttu-id="0fed8-p102">L'agrégation des données qui résulte de la fusion de formulaires peut inclure toutes les données contenues dans les formulaires source et cible, ou seulement une partie de ces données. Les opérations par défaut sont les suivantes.</span><span class="sxs-lookup"><span data-stu-id="0fed8-p102">The aggregation of data that results from merging forms can include all of the data that is contained in the source and target forms, or only a portion of the original data. The default operations are the following.</span></span>
  
- <span data-ttu-id="0fed8-p103">Pour les éléments répétés, les données sont insérées dans l'emplacement correspondant sur le document cible. Cela se produit lorsque l'attribut **MaxOccurs** de l'élément de destination est supérieur à 1.</span><span class="sxs-lookup"><span data-stu-id="0fed8-p103">For repeating elements, data is inserted at a matching location in the target document. This happens when the **MaxOccurs** attribute of the destination element is greater than 1.</span></span> 
    
- <span data-ttu-id="0fed8-112">Pour les éléments non répétés (c'est-à-dire ceux où **MaxOccurs** est égal à 1), les attributs des éléments source sont ajoutés aux attributs existants de l'élément de destination.</span><span class="sxs-lookup"><span data-stu-id="0fed8-112">For non-repeating elements (that is, for elements where **MaxOccurs** is "1"), the attributes of the source elements are added to the existing attributes of the destination element.</span></span> 
    
## <a name="creating-a-custom-transform"></a><span data-ttu-id="0fed8-113">Création d'une transformation personnalisée</span><span class="sxs-lookup"><span data-stu-id="0fed8-113">Creating a Custom Transform</span></span>

<span data-ttu-id="0fed8-p104">L'opération de fusion par défaut des formulaires fonctionne bien pour les formulaires basés sur le même schéma XML. Dans certains cas, cependant, vous souhaiterez fusionner des formulaires basés sur des schémas différents ou remplacer l'opération de fusion par défaut pour des formulaires qui sont basés sur le même schéma. Pour ces scénarios, vous pouvez créer une transformation XSL qui contient des instructions d'agrégation pour l'opération de fusion. La transformation est appliquée au moment de la fusion pour créer un document DOM qui contient les informations à importer, avec des annotations qui spécifient la façon d'incorporer ces informations dans le document cible. Ces annotations sont des attributs XML dans l'espace de noms  `http://schemas.microsoft.com/office/InfoPath/2003/aggregation`.</span><span class="sxs-lookup"><span data-stu-id="0fed8-p104">The default operation when merging forms works well for forms that are based on the same XML schema. In some circumstances, however, you may want to merge forms that are based on different schemas or override the default merge operation for forms that are based on the same schema. For these scenarios, you can create an XSL Transform (XSLT), which contains aggregation instructions for the merge operation. The transform is applied at merge time to create a DOM document that contains the information to be imported, together with annotations specifying how to incorporate this information into the target document. These annotations are XML attributes in the namespace  `http://schemas.microsoft.com/office/InfoPath/2003/aggregation`.</span></span>
  
<span data-ttu-id="0fed8-p105">Les attributs XML et leurs valeurs servent d'instructions d'agrégation sur la façon dont chaque nœud est fusionné dans le document XML de destination. Ces attributs sont décrits dans les sections suivantes.</span><span class="sxs-lookup"><span data-stu-id="0fed8-p105">The XML attributes and their values serve as aggregation instructions on how each node is merged with the destination XML document. These attributes are described in the following sections.</span></span>
  
### <a name="select"></a><span data-ttu-id="0fed8-121">select</span><span class="sxs-lookup"><span data-stu-id="0fed8-121">select</span></span>

<span data-ttu-id="0fed8-122">L'attribut **agg:select** contient une expression de chemin absolu XPath qui identifie l'élément de destination.</span><span class="sxs-lookup"><span data-stu-id="0fed8-122">The **agg:select** attribute contains an absolute XPath expression which identifies the destination element.</span></span> 
  
### <a name="insert"></a><span data-ttu-id="0fed8-123">insert</span><span class="sxs-lookup"><span data-stu-id="0fed8-123">insert</span></span>

<span data-ttu-id="0fed8-p106">La valeur « insert » pour l'attribut **agg:action** indique à InfoPath d'insérer l'élément source comme enfant de l'élément de destination qui est spécifié par l'attribut **agg:select**. Les enfants de l'élément source sont inclus dans l'opération d'insertion. L'attribut **selectChild** vous permet de sélectionner un certain emplacement pour l'opération d'insertion de nœud. L'attribut **order** permet de spécifier si les éléments source sont insérés avant les éléments de destination existants ou après. La valeur par défaut si l'attribut **order** est absent est « after » (après).</span><span class="sxs-lookup"><span data-stu-id="0fed8-p106">A value of "insert" for the **agg:action** attribute instructs InfoPath to insert the source element as a child of the destination element that is specified by using the **agg:select** attribute. The children of the source element are included in the insert operation. The **selectChild** attribute lets you select a certain location for the insert node operation. The **order** attribute is used to specify whether the source elements are inserted before existing destination elements or after. The default value if the **order** attribute is not present is "after".</span></span> 
  
```XML
<my:field1 agg:select="/my:myFields/my:field1"
 agg:action="insert" agg:order="before">Some Value</my:field1>

```

### <a name="replace"></a><span data-ttu-id="0fed8-129">replace</span><span class="sxs-lookup"><span data-stu-id="0fed8-129">replace</span></span>

<span data-ttu-id="0fed8-130">La valeur « replace » pour l'attribut **agg:action** indique à InfoPath de remplacer chacun des éléments de destination que l'attribut **select** référence par l'élément source.</span><span class="sxs-lookup"><span data-stu-id="0fed8-130">A value of "replace" for the **agg:action** attribute instructs InfoPath to replace each of the destination elements referred to by the **select** attribute with the source element.</span></span> 
  
```XML
<my:field1 agg:select="/my:myFields/my:field1"
 agg:action="replace">Some Value</my:field1>
```

### <a name="mergeattributes"></a><span data-ttu-id="0fed8-131">mergeAttributes</span><span class="sxs-lookup"><span data-stu-id="0fed8-131">mergeAttributes</span></span>

<span data-ttu-id="0fed8-132">Si la valeur de l'attribut **agg:action** est « mergeAttributes », les attributs de l'élément source sont fusionnés avec les attributs de chacun des éléments de destination référencés par l'attribut **select**.</span><span class="sxs-lookup"><span data-stu-id="0fed8-132">If the value of the **agg:action** attribute is "mergeAttributes", the attributes of the source element are merged with the attributes of each of the destination elements referred to by the **select** attribute.</span></span> 
  
```XML
<my:PMAwS agg:action="mergeAttributes"
 agg:select="/my:Root/my:PMAwS">
```

### <a name="delete"></a><span data-ttu-id="0fed8-133">delete</span><span class="sxs-lookup"><span data-stu-id="0fed8-133">delete</span></span>

<span data-ttu-id="0fed8-134">Si la valeur de l'attribut **agg:action** est « delete », chacun des éléments de destination référencés par l'attribut **select** sont supprimés du document de destination.</span><span class="sxs-lookup"><span data-stu-id="0fed8-134">If the value of the **agg:action** attribute is "delete", each of the destination elements referred to by the **select** attribute are deleted from the destination document.</span></span> 
  
```XML
<my:field1 agg:select="/my:myFields/my:field1"
 agg:action="delete"/>
```

<span data-ttu-id="0fed8-p107">En conjonction avec les attributs spécifiés dans l'espace de noms  `http://schemas.microsoft.com/office/InfoPath/2003/aggregation`, vous utilisez l'espace de noms  `http://schemas.microsoft.com/office/infopath/2003/aggregation-target` pour indiquer un objet XSL qui implémente l'interface **IXMLDOMDocument**. La méthode **get-documentElement** est l'un des membres les plus utiles de cette interface.</span><span class="sxs-lookup"><span data-stu-id="0fed8-p107">In conjunction with the attributes specified in the  `http://schemas.microsoft.com/office/InfoPath/2003/aggregation` namespace, you use the  `http://schemas.microsoft.com/office/infopath/2003/aggregation-target` namespace to denote an XSL object that implements the interface **IXMLDOMDocument**. One of the most useful members of this interface is the method **get-documentElement**.</span></span>
  
### <a name="get-documentelement"></a><span data-ttu-id="0fed8-137">get-documentElement</span><span class="sxs-lookup"><span data-stu-id="0fed8-137">get-documentElement</span></span>

<span data-ttu-id="0fed8-p108">La fonction **target:get-documentElement** fournit l'accès au DOM (Document Object Model) du document de destination. Vous pouvez l'utiliser pour changer le fonctionnement de l'opération de fusion basé sur le contenu du document de destination.</span><span class="sxs-lookup"><span data-stu-id="0fed8-p108">The **target:get-documentElement** function provides access to the Document Object Model of the destination document. It can be used to change the way the merge operation works based on the current contents of the destination document.</span></span> 
  
```XML
<xsl:when test="function-available('target:get-documentElement')">
    <xsl:variable name="target" select="target:get-documentElement()" />
    <xsl:if test="not(boolean($target/my:Customer[Name="MyName"]))">
        <my:Customer agg:action="insert" agg:select="/my:MergeForms" />
    </xsl:if>
</xsl:when>

```

## <a name="steps-for-creating-a-custom-merge"></a><span data-ttu-id="0fed8-140">Procédure de création d'une fusion personnalisée</span><span class="sxs-lookup"><span data-stu-id="0fed8-140">Steps for Creating a Custom Merge</span></span>

1. <span data-ttu-id="0fed8-p109">Sélectionnez les types de documents XML source à partir desquels fusionner les données. Collectez un échantillon représentatif de chaque type de document source.</span><span class="sxs-lookup"><span data-stu-id="0fed8-p109">Select the kinds of XML source documents from which you want to merge data. Collect a representative sample of each kind of source document.</span></span>
    
2. <span data-ttu-id="0fed8-p110">Dérivez le schéma XML de chaque type de document source XML pour un formulaire InfoPath existant. Cette étape s'effectue aisément en exportant le schéma XML avec la commande **Exporter les fichiers source** de l'onglet **Publier** de Backstage. Pour les documents XML qui n'ont pas été créés dans InfoPath, vous pouvez utiliser un outil comme Microsoft Visual Studio pour créer un schéma à partir du document XML échantillon, ou créer un formulaire échantillon à partir du document XML dans InfoPath, puis exporter le schéma que InfoPath dérive de la structure du document.</span><span class="sxs-lookup"><span data-stu-id="0fed8-p110">Derive the XML schema for each kind of XML source document for an existing InfoPath form. This step is easily accomplished by exporting the XML schema with the **Export Source Files** command on the **Publish** tab of the Backstage. For XML documents that were not created in InfoPath, you can use a tool such as Microsoft Visual Studio to create a schema from the sample XML document, or you can create a sample form from the XML document in InfoPath, and then export the schema that InfoPath derives from the document structure.</span></span> 
    
3. <span data-ttu-id="0fed8-p111">Identifiez les données que vous voulez fusionner à partir de chaque type de document XML source. Cette étape dépend presque entièrement des exigences de vos formulaires source et destination. Pour certains formulaires, vous souhaiterez copier toutes les données du formulaire source. Pour d'autres, vous souhaiterez seulement un ou deux éléments du document XML sous-jacent au formulaire. Lors de l'identification des données à fusionner, soyez très attentif quant aux documents source et de destination pour assurer la correspondance logique des éléments entre les deux formulaires.</span><span class="sxs-lookup"><span data-stu-id="0fed8-p111">Identify the data that you want to merge from each kind of XML source document. This step will depend almost entirely on the requirements of both your source and destination forms. For some forms, you may want to copy all of the data from the source form. For others, you may want only one or two elements from the form's underlying XML document. When identifying what data that you want to merge, pay extra attention to both the source and destination documents to ensure that the elements map logically between the two forms.</span></span>
    
4. <span data-ttu-id="0fed8-p112">Créez une transformation XSL pour chaque type de document XML source. Cette étape de configuration de la fusion des formulaires est la plus longue. Le but de la transformation XSL est de transformer le document XML source dans un format qui puisse être fusionné dans le formulaire de destination. Lors de la conception de votre transformation, choisissez si vous utilisez la fusion à partir des chemins d'accès aux fichiers XML ou la fusion à partir des instructions d'agrégation InfoPath.</span><span class="sxs-lookup"><span data-stu-id="0fed8-p112">Create an XSL transform for each kind of XML source document. When configuring the merging of your forms, this step will take the most time. The purpose of the XSL transform is to transform the source XML document into a format that can be merged with the destination form. When designing your transform, decide whether you want to use merging from XML location paths, or merging from InfoPath aggregation instructions.</span></span>
    
    <span data-ttu-id="0fed8-p113">Visual Studio est un outil pratique pour créer des transformations XSL. Visual Studio fournit la coloration de la syntaxe et un plan du document. Il propose automatiquement les balises fermantes pour vos éléments XSL, ce qui contribue à réduire les saisies redondantes et les fautes de frappe difficiles à repérer. Vous pouvez également créer des transformations XSL à l'aide d'un éditeur de texte tel que Notepad.</span><span class="sxs-lookup"><span data-stu-id="0fed8-p113">Visual Studio is a convenient tool for creating XSL transforms. Visual Studio provides syntax coloring and a document outline. It also automatically provides closing tags for your XSL elements, which can help decrease redundant typing and hard-to-find spelling errors. You can also create XSL transforms with a text editor such as Notepad.</span></span>
    
    <span data-ttu-id="0fed8-159">Commencez par la transformation d'identité, qui est une simple transformation XSL qui produit en sortie le même fichier XML qu'en entrée :</span><span class="sxs-lookup"><span data-stu-id="0fed8-159">Start with the identity transform, which is simply an XSL transform that outputs the same XML file that is input:</span></span>
    
    ```XML
        <?xml version="1.0"?> 
        <xsl:stylesheet version="1.0" xmlns:xsl="http://www.w3.org/1999/XSL/Transform" 
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

    <span data-ttu-id="0fed8-p114">Ajoutez ensuite des sections de remplacement pour les éléments auxquels vous souhaitez ajouter un traitement spécial. Par exemple, ce modèle remplace un élément  `<src:Task>` par un élément  `<my:field1>` et affecte la valeur « replace » à l'attribut **agg:action**.</span><span class="sxs-lookup"><span data-stu-id="0fed8-p114">Then add overriding template sections for the elements you want to add special handling for. For example, this template changes a  `<src:Task>` element into a  `<my:field1>` element and sets the value of the **agg:action** attribute to "replace".</span></span> 
    
    ```XML
        <xsl:template match="src:Task"> 
            <my:field1 agg:select="/my:myFields/my:field1" agg:action="replace"> 
                <xsl:value-of select="."/> 
            </my:field1> 
        </xsl:template>
    ```

5. <span data-ttu-id="0fed8-p115">Ajoutez les fichiers de transformation XSL et les fichiers de schéma dans le modèle de formulaire. Après avoir dérivé les schémas de chaque type de document source et créé une transformation XSL pour convertir chaque type de document afin que InfoPath puisse fusionner ses données, ajoutez-les en tant que ressources à votre formulaire. Cliquez sur **Fichiers de ressources** sur l'onglet **Données**, puis cliquez sur **Ajouter** dans la boîte de dialogue **Fichiers de ressources**, accédez à votre fichier de schéma ou de transformation XSL, puis cliquez sur **OK**. Effectuez cette opération pour chaque fichier de schéma et de transformation XSL que vous avez créé.</span><span class="sxs-lookup"><span data-stu-id="0fed8-p115">Add the XSL transform files and schema files in the form template. After you have derived schemas for each kind of source document and created an XSL transform to convert each document type so that InfoPath can merge its data, add them to as resources to your form. Click **Resource Files** on the **Data** tab, and then click **Add** in the **Resource Files** dialog box, browse to your schema or XSL transform file, and then click **OK**. Do this to for each schema file and XSL transform file that you created.</span></span>
    
    <span data-ttu-id="0fed8-p116">Si les schémas que vous ajoutez utilisent l'attribut **targetNamespace**, vous de devez ajouter un élément propriété au fichier .xsf du formulaire afin que InfoPath connaisse l'espace de noms du schéma. Pour accéder à ce fichier, cliquez sur l'onglet **Fichier**, cliquez sur **Publier**, puis cliquez sur **Exporter les fichiers source**. Sélectionnez un emplacement pour les fichiers, puis cliquez sur **OK**. Enfin, fermez le modèle de formulaire InfoPath en cours de conception.</span><span class="sxs-lookup"><span data-stu-id="0fed8-p116">If the schemas that you add use the **targetNamespace** attribute, you must add a property element to the form's .xsf file so that InfoPath knows the namespace of the schema. To access this file, click the **File** tab, click **Publish**, and then click **Export Source Files**. Select a location for the files, and then click **OK**. Then close the InfoPath form template that you are designing.</span></span>
    
    <span data-ttu-id="0fed8-p117">Accédez à l'emplacement que vous avez spécifié pour les fichiers extraits et recherchez le fichier portant l'extension de nom .xsf. Généralement, ce fichier s'appelle manifest.xsf. Ouvrez-le dans Notepad, recherchez la balise  `<xsf:file>` qui correspond à votre schéma, et ajoutez un élément propriété « namespace » pour spécifier l'espace de noms cible **targetNamespace** comme illustré dans l'exemple suivant.</span><span class="sxs-lookup"><span data-stu-id="0fed8-p117">Browse to the location that you specified for the extracted files and find the file that has an .xsf file name extension. Usually, this file is called manifest.xsf. Open the file in Notepad, find the  `<xsf:file>` tag that corresponds to your schema, and add a "namespace" property element to specify the **targetNamespace** as shown in the following example.</span></span> 
    
    ```xml
        <xsf:file name="IndvTasks.xsd"> 
            <xsf:fileProperties> 
                <xsf:property name="fileType" type="string" value="Resource" /> 
                <xsf:property name="namespace" type="string" 
                value="urn:office-microsoft-com:InfoPath-designer-aggregation-IndStatusReport" /> 
            </xsf:fileProperties> 
        </xsf:file>
    ```

6. <span data-ttu-id="0fed8-173">La dernière étape de préparation de votre formulaire pour prendre en charge la fusion personnalisée consiste à mettre à jour l’élément **importParameters** dans le fichier .xsf associé au formulaire.</span><span class="sxs-lookup"><span data-stu-id="0fed8-173">The last step in preparing your form to support custom merging is to update the **importParameters** element in the .xsf file associated with the form.</span></span> 

    <span data-ttu-id="0fed8-174">Tout d’abord, recherchez le `<xsf:importParameters>` balise dans le fichier .xsf.</span><span class="sxs-lookup"><span data-stu-id="0fed8-174">First, find the  `<xsf:importParameters>` tag in the .xsf file.</span></span> <span data-ttu-id="0fed8-175">Pour chaque schéma paire/transformation XSL que vous avez créé pour votre formulaire, ajoutez un élément **xsf : importSource** à l’élément **xsf : importParameters** : `<xsf:importParameters enabled="yes"> <xsf:importSource name="" schema="IndvTasks.xsd" transform="ImportTasks.xsl"></xsf:importSource> </xsf:importParameters>`.</span><span class="sxs-lookup"><span data-stu-id="0fed8-175">For each schema/XSL transform pair you have created for your form, add an **xsf:importSource** element to the **xsf:importParameters** element:  `<xsf:importParameters enabled="yes"> <xsf:importSource name="" schema="IndvTasks.xsd" transform="ImportTasks.xsl"></xsf:importSource> </xsf:importParameters>`.</span></span> 
    
    <span data-ttu-id="0fed8-176">L’attribut **name** de l’élément **xsf : importSource** contient le nom du modèle de formulaire qui peut se trouver dans un document XML source.</span><span class="sxs-lookup"><span data-stu-id="0fed8-176">The **name** attribute of the **xsf:importSource** element contains the form template's name that may be found in a source XML document.</span></span> <span data-ttu-id="0fed8-177">En règle générale, vous laissez cette zone vide.</span><span class="sxs-lookup"><span data-stu-id="0fed8-177">Usually, you can leave this empty.</span></span> <span data-ttu-id="0fed8-178">L’attribut **schema** contient le nom d’un fichier de schéma que vous avez ajouté au modèle de formulaire à l’étape précédente.</span><span class="sxs-lookup"><span data-stu-id="0fed8-178">The **schema** attribute contains the name of a schema file that you added to the form template in the previous step.</span></span> <span data-ttu-id="0fed8-179">Enfin, l’attribut **transform** contient le nom de la transformation XSL que vous souhaitez utiliser pour convertir les formulaires conformément au schéma.</span><span class="sxs-lookup"><span data-stu-id="0fed8-179">Finally, the **transform** attribute contains the name of the XSL transform that you want to use to convert forms that conform to the schema.</span></span> 
    
    <span data-ttu-id="0fed8-180">Vous pouvez utiliser une transformation personnalisée avec l’événement [de fusion](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Merge.aspx) ou sur son propre.</span><span class="sxs-lookup"><span data-stu-id="0fed8-180">You can use a custom transform either with the [Merge](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Merge.aspx) event or on its own.</span></span> 
    
## <a name="creating-a-custom-merge-in-code"></a><span data-ttu-id="0fed8-181">Création d'une fusion personnalisée dans le code</span><span class="sxs-lookup"><span data-stu-id="0fed8-181">Creating a Custom Merge in Code</span></span>

<span data-ttu-id="0fed8-182">La fusion personnalisée avec code est prise en charge par le gestionnaire d'événements [Merge](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Merge.aspx) , avec son attribut **useScriptHandler** correspondant dans l'élément **importParameters** du fichier .xsf associé au formulaire.</span><span class="sxs-lookup"><span data-stu-id="0fed8-182">Custom merging with code is supported by using the [Merge](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Merge.aspx) event handler, with its corresponding **useScriptHandler** attribute of the **importParameters** element in the .xsf file associated with the form.</span></span> 

<span data-ttu-id="0fed8-183">Dans le code managé, vous pouvez activer l'événement [Merge](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Merge.aspx) en activant la case à cocher **Fusionner à l'aide d'un code personnalisé**, puis en cliquant sur le bouton **Modifier**, dans la catégorie **Avancé** de la boîte de dialogue **Options de formulaire** disponible à partir de Backstage.</span><span class="sxs-lookup"><span data-stu-id="0fed8-183">In managed code, you can enable the [Merge](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Merge.aspx) event by checking the box **Merge using custom code**, and then clicking the **Edit** button, in the **Advanced** category of the **Form Options** dialog box available from the Backstage.</span></span> 
  

