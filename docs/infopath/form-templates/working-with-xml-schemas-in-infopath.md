---
title: Utilisation des schémas XML dans InfoPath
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: c1d70e9f-b9fc-7bdb-107e-d0cd8191607b
description: Un modèle de formulaire que vous créez avec Microsoft InfoPath utilise un schéma XML (XSD) pour effectuer une validation de la structure et des données du code XML qui est en entrée, en modification et en sortie d'un formulaire InfoPath. Chaque modèle de formulaire créé dans le concepteur de formulaires InfoPath contient au moins un fichier de schéma XSD (.xsd) qui est utilisé pour la validation lors de l'exécution.
ms.openlocfilehash: 6921a2206c098992a0a24e85c263992a0e2c98b1
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19782484"
---
# <a name="working-with-xml-schemas-in-infopath"></a><span data-ttu-id="721b3-104">Utilisation des schémas XML dans InfoPath</span><span class="sxs-lookup"><span data-stu-id="721b3-104">Working with XML Schemas in InfoPath</span></span>

<span data-ttu-id="721b3-p102">Un modèle de formulaire que vous créez avec Microsoft InfoPath utilise un schéma XML (XSD) pour effectuer une validation de la structure et des données du code XML qui est en entrée, en modification et en sortie d'un formulaire InfoPath. Chaque modèle de formulaire créé dans le concepteur de formulaires InfoPath contient au moins un fichier de schéma XSD (.xsd) qui est utilisé pour la validation lors de l'exécution.</span><span class="sxs-lookup"><span data-stu-id="721b3-p102">A form template that you create with Microsoft InfoPath uses an XML Schema (XSD) to perform structural and data validation on the XML that is input, edited, and output from an InfoPath form. Every form template created in the InfoPath form designer contains at least one XSD schema file (.xsd) that is used for validation at run time.</span></span>
  
> [!NOTE]
> <span data-ttu-id="721b3-p103">[!REMARQUE] Les informations contenues dans cette rubrique s'appliquent aux modèles de formulaire conçus pour être utilisés dans l'éditeur d'InfoPath. Les modèles de formulaire compatibles avec un navigateur ont des conditions requises plus strictes quant au schéma XSD. Pour plus d'informations, voir la documentation disponible sur MSDN sur les schémas XML dans les modèles de formulaire compatibles avec un navigateur.</span><span class="sxs-lookup"><span data-stu-id="721b3-p103">The information contained in this topic applies to form templates designed for use in the InfoPath editor. Browser-compatible form templates have stricter XSD Schema requirements. For more information, see the documentation about XML Schemas in browser-compatible form templates available on MSDN.</span></span> 
  
## <a name="using-externally-authored-xml-schemas"></a><span data-ttu-id="721b3-110">Utilisation de schémas XML créés en externe</span><span class="sxs-lookup"><span data-stu-id="721b3-110">Using Externally-authored XML Schemas</span></span>

<span data-ttu-id="721b3-111">Pour charger un fichier de schéma XSD qui a été créé en dehors d'InfoPath, procédez selon les étapes suivantes.</span><span class="sxs-lookup"><span data-stu-id="721b3-111">To load an XSD schema file that was authored outside of InfoPath, follow these steps.</span></span>
  
### <a name="to-create-a-form-template-based-on-an-external-schema"></a><span data-ttu-id="721b3-112">Pour créer un modèle de formulaire basé sur un schéma externe</span><span class="sxs-lookup"><span data-stu-id="721b3-112">To create a form template based on an external schema</span></span>

1. <span data-ttu-id="721b3-113">Dans Backstage, cliquez sur **Nouveau**, cliquez sur **Fichier ou schéma XML** sous **Modèles de formulaires avancés**, puis cliquez sur **Modifier ce formulaire**.</span><span class="sxs-lookup"><span data-stu-id="721b3-113">In the Backstage, click **New**, click **XML or Schema** under **Advanced Form Templates**, and then click **Design This Form**.</span></span>
    
2. <span data-ttu-id="721b3-114">Dans l' **Assistant Source de données**, spécifiez le fichier de schéma XSD que vous voulez utiliser, puis cliquez sur **Suivant** et continuez avec les pages suivantes de l'Assistant.</span><span class="sxs-lookup"><span data-stu-id="721b3-114">In the **Data Source Wizard**, specify the XSD schema file you want to use, and then click **Next** and complete the remaining pages of the wizard.</span></span> 
    
## <a name="unsupported-xsd-constructs"></a><span data-ttu-id="721b3-115">Constructions XSD non prises en charge</span><span class="sxs-lookup"><span data-stu-id="721b3-115">Unsupported XSD Constructs</span></span>

<span data-ttu-id="721b3-p104">Les sections suivantes décrivent les constructions XSD qu'InfoPath ne peut pas gérer lors de l'exécution. Évitez ces constructions lors de la création d'un modèle de formulaire dans le concepteur de formulaires InfoPath.</span><span class="sxs-lookup"><span data-stu-id="721b3-p104">The following sections describe XSD constructs that InfoPath cannot handle at run time. Avoid these constructs when creating a form template in the InfoPath form designer.</span></span>
  
## <a name="entity-and-entities-types"></a><span data-ttu-id="721b3-118">Types ENTITY et ENTITIES</span><span class="sxs-lookup"><span data-stu-id="721b3-118">ENTITY and ENTITIES Types</span></span>

<span data-ttu-id="721b3-p105">Les types **ENTITY** et **ENTITIES** requièrent une définition de type de document (DTD) pour la validation, ce qu'InfoPath ne prend pas en charge. InfoPath ne vous permet pas de concevoir un modèle de formulaire basé sur un tel schéma et affiche un message d'erreur recommandant de remplacer le type **ENTITY** par le type **NCName** dont **ENTITY** est dérivé.</span><span class="sxs-lookup"><span data-stu-id="721b3-p105">The **ENTITY** and **ENTITIES** types require a document type definition (DTD) for validation, which InfoPath does not support. InfoPath does not allow you to design a form template against such a schema and displays an error message that recommends changing the **ENTITY** type to the **NCName** type from which **ENTITY** derives.</span></span> 
  
> [!NOTE]
>  <span data-ttu-id="721b3-121">[!REMARQUE]  Si vous créez manuellement un modèle de formulaire InfoPath en dehors du mode Création et qu'il utilise un schéma XSD incluant les types **ENTITY** et **ENTITIES**, le modèle de formulaire peut éventuellement fonctionner à l'exécution si le fichier Template.xml contient la DTD requise pour ces types.</span><span class="sxs-lookup"><span data-stu-id="721b3-121">If you manually author an InfoPath form template outside of design mode, and it uses an XSD that includes **ENTITY** and **ENTITIES** types, the form template may work at run time if the Template.xml file contains the required DTD for these types.</span></span> 
  
## <a name="required-xsdany-element"></a><span data-ttu-id="721b3-122">Élément xsd:any requis</span><span class="sxs-lookup"><span data-stu-id="721b3-122">Required xsd:any Element</span></span>

<span data-ttu-id="721b3-p106">Une occurrence d'un élément générique **xsd:any**, c'est-à-dire une occurrence d'un élément **xsd:any** avec une valeur pour l'attribut **minOccurs** supérieure à zéro (paramètre « xsd:any » requis), empêche InfoPath de créer de façon déterministe une instance valide de fragment de schéma. InfoPath doit pouvoir créer une instance valide lors de la génération d'un formulaire qui utilise ce fragment de schéma. Dans le cadre de l'exécution de l' **Assistant Source de données**, les schémas avec des éléments **xsd:any** requis vous obligent à choisir l'élément de schéma que vous voulez utiliser à la place de l'élément **xsd:any** requis.</span><span class="sxs-lookup"><span data-stu-id="721b3-p106">An occurrence of an **xsd:any** wildcard element, that is, an occurrence of an **xsd:any** element with a **minOccurs** attribute value greater than zero ("required any"), prevents InfoPath from deterministically creating a valid instance for this schema fragment. InfoPath must be able to create a valid instance when generating a form that uses this schema fragment. As part of running the **Data Source Wizard**, schemas with required **xsd:any** elements require you to choose which schema element you want to use in place of the required **xsd:any** element.</span></span> 
  
## <a name="elements-with-an-abstract-complex-type"></a><span data-ttu-id="721b3-126">Éléments avec un type complexe abstrait</span><span class="sxs-lookup"><span data-stu-id="721b3-126">Elements with an Abstract Complex Type</span></span>

<span data-ttu-id="721b3-p107">Le mode Création d'InfoPath prend en charge la conception d'un modèle de formulaire basé sur des schémas utilisant des types complexes abstraits. Par exemple, si un élément nommé  `shippingAddress` a un type complexe abstrait nommé  `address` qui a deux dérivations,  `USAddress` et  `CanadianAddress`, InfoPath traite les instances de  `shippingAddress` comme un choix entre  `shippingAddress` avec le type  `USAddress` et  `shippingAddress` avec le type  `CanadianAddress`. Dans cet exemple, si les schémas fournis ne contiennent pas de types qui dérivent de cette adresse, InfoPath demande un schéma supplémentaire qui répond à cette condition requise.</span><span class="sxs-lookup"><span data-stu-id="721b3-p107">InfoPath design mode supports designing a form template against schemas that use abstract complex types. For example, if an element named  `shippingAddress` has an abstract complex type named  `address` that has two derivations,  `USAddress` and  `CanadianAddress`, InfoPath treats any instance of  `shippingAddress` as a choice between  `shippingAddress` with type  `USAddress` and  `shippingAddress` with type  `CanadianAddress` . In this example, if the provided schemas contain no types that derive from address, then InfoPath requests an additional schema that fulfills this requirement.</span></span> 
  
## <a name="xsd-constructs-with-reduced-functionality"></a><span data-ttu-id="721b3-130">Constructions XSD avec une fonctionnalité réduite</span><span class="sxs-lookup"><span data-stu-id="721b3-130">XSD Constructs with Reduced Functionality</span></span>

<span data-ttu-id="721b3-131">Les sections suivantes décrivent des constructions XSD qui ont une fonctionnalité réduite lorsqu'ils sont utilisés pour créer un modèle de formulaire dans le concepteur de formulaires InfoPath.</span><span class="sxs-lookup"><span data-stu-id="721b3-131">The following sections describe XSD constructs that have reduced functionality when used to create a form template in the InfoPath form designer.</span></span>
  
## <a name="substitution-groups"></a><span data-ttu-id="721b3-132">Groupes de substitution</span><span class="sxs-lookup"><span data-stu-id="721b3-132">Substitution Groups</span></span>

<span data-ttu-id="721b3-p108">Tous les membres du groupe de substitution apparaissent dans le volet Office **Champs**. InfoPath représente les possibilités de substitution comme un choix de tous les groupes de substitution (y compris l'élément de définition s'il n'est pas abstrait). S'il n'existe pas de groupes de substitution pour un élément abstrait, InfoPath vous invite à fournir un schéma contenant au moins un élément qui est un groupe de substitution.</span><span class="sxs-lookup"><span data-stu-id="721b3-p108">All members of the substitution group appear in the **Fields** task pane. InfoPath represents the substitution possibilities as a choice of all the substitution groups (including the defining element, if it is not abstract). If there are no substitution groups for an abstract element, InfoPath prompts you to provide a schema that contains at least one element that is a substitution group.</span></span> 
  
## <a name="unbounded-choice-elements"></a><span data-ttu-id="721b3-136">Éléments choice non liés</span><span class="sxs-lookup"><span data-stu-id="721b3-136">Unbounded Choice Elements</span></span>

<span data-ttu-id="721b3-137">Le fragment de schéma suivant montre un élément choice non lié :</span><span class="sxs-lookup"><span data-stu-id="721b3-137">The following schema fragment shows an unbounded choice element:</span></span>
  
```XML
<xsd:choice maxOccurs="unbounded"> 
    <xsd:element name="my_element_1"/> 
    <xsd:element name="my_element_2"/> 
</xsd:choice> 

```

<span data-ttu-id="721b3-p109">InfoPath affiche les éléments choice extensibles en tant que choix extensibles dans le volet Office **Champs**. Il existe un contrôle **Groupe de choix extensible**, que vous pouvez utiliser pour représenter la liste hétérogène définie par l'élément choice extensible dans le schéma XSD.</span><span class="sxs-lookup"><span data-stu-id="721b3-p109">InfoPath displays repeating choice elements as repeating choices in the **Fields** task pane. There is a **Repeating Choice Group** control that you can use to represent the heterogeneous list defined by the repeating choice element in the XSD.</span></span> 
  
## <a name="repeating-sequence"></a><span data-ttu-id="721b3-140">Séquence extensible</span><span class="sxs-lookup"><span data-stu-id="721b3-140">Repeating Sequence</span></span>

<span data-ttu-id="721b3-141">Le fragment de schéma suivant montre une séquence extensible :</span><span class="sxs-lookup"><span data-stu-id="721b3-141">The following schema fragment shows a repeating sequence:</span></span>
  
```XML
<xsd:sequence maxOccurs="unbounded"> 
    <xsd:element name="my_element_1"/> 
    <xsd:element name="my_element_2" minOccurs="0"/> 
</xsd:sequence> 

```

<span data-ttu-id="721b3-142">Tant que la séquence extensible contient un élément requis, InfoPath charge le schéma XSD sans le modifier et vous permet de lier les contrôles de la section extensible à la séquence extensible.</span><span class="sxs-lookup"><span data-stu-id="721b3-142">As long as the repeating sequence contains a required element, InfoPath loads the XSD without modifying it and allows you to bind repeating section controls to the repeating sequence.</span></span>
  
## <a name="choice-of-model-groups"></a><span data-ttu-id="721b3-143">Choix de groupes de modèles</span><span class="sxs-lookup"><span data-stu-id="721b3-143">Choice of Model Groups</span></span>

<span data-ttu-id="721b3-144">Le fragment de schéma suivant montre l'élément choice contenant plusieurs groupes de modèles :</span><span class="sxs-lookup"><span data-stu-id="721b3-144">The following schema fragment shows the choice element containing several model groups:</span></span>
  
```XML
<xsd:choice> 
    <xsd:element name="my_element_1"/> 
    <xsd:sequence> 
        <xsd:element name="my_element_2"/> 
        <xsd:element name="my_element_3"/> 
    </xsd:sequence> 
</xsd:choice> 

```

<span data-ttu-id="721b3-p110">Le mode Création d'InfoPath prend en charge de telles constructions XSD sans requérir de modifications par le concepteur du formulaire. Comme InfoPath ne modifie pas la signification du schéma, il simplifie la construction choice ci-dessus en un choix unique réduit équivalent dans le volet Office **Champs**.</span><span class="sxs-lookup"><span data-stu-id="721b3-p110">InfoPath design mode supports such XSD constructs without requiring any modification by the form designer. While InfoPath does not modify the meaning of the schema, it simplifies the choice construct above into an equivalent collapsed single choice in the **Fields** task pane.</span></span> 
  
## <a name="optional-sibling-with-same-qualified-name"></a><span data-ttu-id="721b3-147">Frère facultatif avec le même nom qualifié</span><span class="sxs-lookup"><span data-stu-id="721b3-147">Optional Sibling with Same Qualified Name</span></span>

<span data-ttu-id="721b3-148">Le fragment de schéma suivant montre un frère facultatif avec le même nom qualifié (`QName`) :</span><span class="sxs-lookup"><span data-stu-id="721b3-148">The following schema fragment shows an optional sibling with same qualified name (`QName`):</span></span>
  
```xml
<xsd:sequence> 
    <xsd:element name="my_element_1" minOccurs="0"/> 
    <xsd:element name="my_element_2"/> 
            <xsd:element name="my_element_1"/> 
</xsd:sequence> 

```

<span data-ttu-id="721b3-p111">Les expressions **XPath** pour ces nœuds peuvent être complexes car chaque instance XML potentielle doit être prise en compte dans le concepteur de formulaires d'InfoPath. InfoPath n'expose pas les composants du schéma pour lesquels il peut avoir rencontré des difficultés lors de la création des liaisons **XPath** correctes. Des avertissements apparaissent à propos des parties du schéma qui sont ignorées.</span><span class="sxs-lookup"><span data-stu-id="721b3-p111">**XPath** expressions for these nodes can be complex because every potential XML instance must be accounted for in the InfoPath form designer. InfoPath does not expose parts of the schema for which it may have difficulty creating correct **XPath** bindings. Warnings appear regarding the portions of the schema that are ignored.</span></span> 
  
## <a name="xsd-constructs-with-special-meaning-in-infopath"></a><span data-ttu-id="721b3-152">Constructions XSD avec une signification spéciale dans InfoPath</span><span class="sxs-lookup"><span data-stu-id="721b3-152">XSD Constructs with Special Meaning in InfoPath</span></span>

<span data-ttu-id="721b3-p112">Les sections suivantes décrivent des constructions XSD qui ont une signification spéciale lorsqu'elles sont utilisées dans la création d'un modèle de formulaire en mode Création. Ces sections décrivent comment vous pouvez utiliser les constructions dans votre schéma pour permettre certains comportements.</span><span class="sxs-lookup"><span data-stu-id="721b3-p112">The following sections describe XSD constructs that have special meaning when used in creating a form template in design mode. These sections describe how you can use the constructs in your schema to enable certain behaviors.</span></span>
  
## <a name="adding-new-element-fields-and-groups-with-the-fields-task-pane"></a><span data-ttu-id="721b3-155">Ajout de nouveaux champs et groupes d'éléments avec le volet Office Champs</span><span class="sxs-lookup"><span data-stu-id="721b3-155">Adding New Element Fields and Groups with the Fields Task Pane</span></span>

<span data-ttu-id="721b3-p113">Vous pouvez construire votre schéma de façon à pouvoir utiliser le volet Office **Champs** pour ajouter de nouveaux champs et groupes d'éléments à un élément lors de la conception. Pour cela, vous déclarez un élément dans votre schéma avec un élément **xsd:any** facultatif non lié, qui spécifie l'attribut namespace avec la valeur générique **##any**. Ensuite, en mode Création, vous pouvez utiliser le volet Office **Champs** pour ajouter de nouveaux champs et groupes d'éléments à cet élément. Par exemple, vous pouvez ajouter un nouveau contenu à l'élément suivant :</span><span class="sxs-lookup"><span data-stu-id="721b3-p113">You can construct your schema so that you can use the **Fields** task pane to add new element fields and groups to an element at design time. To do so, you declare an element in your schema with an optional, unbounded **xsd:any** element that specifies the namespace attribute with the **##any** wildcard. Then, in design mode, you can use the **Fields** task pane to add new element fields and groups to that element. For example, you could add new content to the following element:</span></span> 
  
```XML
<xsd:element name="open"> 
    <xsd:complexType> 
         <xsd:sequence> 
             <xsd:any minOccurs="0" maxOccurs="unbounded" namespace="##any"processContents="lax"/> 
         </xsd:sequence> 
    </xsd:complexType> 
</xsd:element> 

```

## <a name="adding-new-attribute-fields-with-the-fields-task-pane"></a><span data-ttu-id="721b3-160">Ajout de nouveaux champs d'attribut avec le volet Office Champs</span><span class="sxs-lookup"><span data-stu-id="721b3-160">Adding New Attribute Fields with the Fields Task Pane</span></span>

<span data-ttu-id="721b3-p114">De la même façon que dans le cas d'un élément, vous pouvez déclarer un attribut avec un élément **anyAttribute** dont l'attribut namespace est spécifié avec la valeur générique **##any**. Lors de la conception, vous pouvez utiliser le volet Office **Champs** pour ajouter un nouveau contenu à cet attribut du schéma.</span><span class="sxs-lookup"><span data-stu-id="721b3-p114">Similarly to the element case, you can declare an attribute with an **anyAttribute** element that has the namespace attribute specified as the **##any** wildcard. At design time, you can use the **Fields** task pane to add new content to that schema attribute.</span></span> 
  
```XML
<xsd:element name="open"> 
    <xsd:complexType> 
        <xsd:anyAttribute namespace="##any" processContents="lax"/> 
    </xsd:complexType> 
</xsd:element> 

```

## <a name="storing-xml-signatures-in-the-data-source"></a><span data-ttu-id="721b3-163">Stockage de signatures XML dans la source de données</span><span class="sxs-lookup"><span data-stu-id="721b3-163">Storing XML Signatures in the Data Source</span></span>

<span data-ttu-id="721b3-p115">Pour permettre aux utilisateurs de signer numériquement un formulaire lors de l'exécution, le schéma de la source de données doit déclarer un élément nommé « signature » pour stocker les informations des signatures numériques XML qui sont créées lorsqu'un utilisateur signe le formulaire. Vous effectuez cette déclaration à l'aide de l'élément **xsd:any** avec l'attribut namespace spécifié en tant qu'espace de noms des signatures XML avec un caractère générique, comme suit : "http://www.w3c.org/2000/09/xmldsig#"</span><span class="sxs-lookup"><span data-stu-id="721b3-p115">To enable users to digitally sign a form at run time, the schema of the data source must declare an element named signature for storing the XML Signatures (digital signature) information that is created when a user signs the form. You make this declaration by using the **xsd:any** element with the namespace attribute specified as the XML Signatures namespace with a wildcard character, as follows: "http://www.w3c.org/2000/09/xmldsig#"</span></span> 
  
```XML
<xsd:element name="signature"> 
    <xsd:complexType> 
        <xsd:sequence> 
            <xsd:any namespace="http://www.w3c.org/2000/09/xmldsig#"  
             processContents="lax" minOccurs="0" maxOccurs="unbounded"/> 
        <xsd:sequence> 
    </xsd:complexType> 
</xsd:element> 

```

## <a name="binding-a-field-to-a-rich-text-box-control"></a><span data-ttu-id="721b3-166">Liaison d'un champ avec un contrôle de zone de texte enrichi</span><span class="sxs-lookup"><span data-stu-id="721b3-166">Binding a Field to a Rich Text Box Control</span></span>

 <span data-ttu-id="721b3-p116">Les contrôles **Zone de texte enrichi** d'InfoPath génèrent du code XHTML générique ; par conséquent, votre schéma doit spécifier qu'un nombre quelconque de textes et de nœuds XHTML est valide dans le code XML de l'instance du formulaire. Vous pouvez effectuer cette spécification avec la construction XSD suivante :</span><span class="sxs-lookup"><span data-stu-id="721b3-p116">**Rich Text Box** controls in InfoPath generate generic XHTML; consequently, your schema must specify that any number of text and XHTML nodes is valid in the XML of the form instance. You can achieve this specification with the following XSD construct:</span></span> 
  
```XML
<xsd:element name="xhtml"> 
    <xsd:complexType mixed="true"> 
        <xsd:sequence> 
            <xsd:any minOccurs="0" maxOccurs="unbounded" namespace="http://www.w3.org/1999/xhtml" processContents="lax"/> 
        </xsd:sequence> 
    </xsd:complexType> 
</xsd:element> 

```

> [!NOTE]
> <span data-ttu-id="721b3-p117">[!REMARQUE] InfoPath ne modifie jamais le contenu du fichier de schéma (.xsd), mais il peut déduire de façon logique un sous-ensemble de celui-ci à des fins de conception. Le fichier de schéma est toujours laissé intact dans le modèle de formulaire lors de la conception et lors de l'exécution.</span><span class="sxs-lookup"><span data-stu-id="721b3-p117">InfoPath never modifies the content of the schema file (.xsd), but it may logically infer a subset of it for design purposes. The schema file is always untouched within the form template at both design time and run time.</span></span> 
  
## <a name="debugging-common-xsd-errors"></a><span data-ttu-id="721b3-171">Débogage des erreurs XSD courantes</span><span class="sxs-lookup"><span data-stu-id="721b3-171">Debugging Common XSD Errors</span></span>

<span data-ttu-id="721b3-p118">Si vous chargez des fichiers XSD créés en externe pour créer des modèles de formulaire dans le concepteur de formulaires d'InfoPath, vous êtes susceptibles de recevoir deux types de messages d'erreur : des messages d'erreur MSXML ou des messages d'erreur InfoPath. Les messages d'erreur MSXML apparaissent dans la section **Détails** d'une boîte de dialogue de message d'erreur InfoPath, et ils commencent toujours par une référence au nom ou au chemin d'accès du fichier de schéma qui a déclenché l'erreur. Certaines constructions de schéma XSD valides ne sont pas prises en charge par InfoPath ; celles-ci sont présentées dans la section Constructions XSD non prises en charge. Les sections suivantes décrivent certaines erreurs courantes qui provoquent l'échec du chargement correct de schémas dans InfoPath.</span><span class="sxs-lookup"><span data-stu-id="721b3-p118">If you load externally authored XSD files to create form templates in the InfoPath form designer, you may receive either of two types of error messages: MSXML error messages or InfoPath error messages. MSXML error messages appear in the **Details** section of an InfoPath error message dialog box, and they always begin with a reference to the name or path of the schema file that is raising the error. Some valid XSD schema constructs are not supported by InfoPath; these are discussed in the Unsupported XSD Constructs section. The following sections describe some common errors that can cause schemas to fail to load successfully in InfoPath.</span></span> 
  
## <a name="the-xsd-namespace-declaration"></a><span data-ttu-id="721b3-176">La déclaration d'espace de noms XSD</span><span class="sxs-lookup"><span data-stu-id="721b3-176">The XSD Namespace Declaration</span></span>

<span data-ttu-id="721b3-p119">De façon similaire à tous les standards W3C, les schémas XML (XSD) ont fait l'objet d'un long processus de révision avant de devenir une recommandation. Il a existé de nombreuses versions de travail et par conséquent, de nombreux fichiers XSD ont été écrits sur la base de ces standards en cours d'évolution. Pendant ce processus, Microsoft a créé un langage de schéma propriétaire appelé XDR (XML-Data Reduced), qui a été inclus dans MSXML 3.0. À partir de MSXML 4.0, Microsoft XML Core Services prend en charge la totalité de la recommandation de XSD. De nombreux programmes de création de schémas n'ont pas attendu que XSD devienne une recommandation complète. Les versions antérieures de ces programmes sont susceptibles de produire des fichiers XSD obsolètes, que l'infrastructure MSXML 5.0, dont dépend InfoPath, ne prend pas en charge.</span><span class="sxs-lookup"><span data-stu-id="721b3-p119">Similar to all W3C standards, XML Schemas (XSD) went through a lengthy review process on its way to becoming a recommendation. There were many working drafts, and consequently, many XSD files were written based on these evolving standards. During this process, Microsoft created a proprietary schema language called XML-Data Reduced (XDR) that was included with MSXML 3.0. Starting with the release of MSXML 4.0, Microsoft XML Core Services supports the full recommendation of XSD. Many programs for creating schemas did not wait for XSD to become a full recommendation. Older versions of these programs may produce outdated XSD files that the MSXML 5.0 infrastructure, on which InfoPath depends, does not support.</span></span>
  
<span data-ttu-id="721b3-183">Pour garantir qu'un fichier XSD prend en charge la recommandation XSD complète, il doit contenir la déclaration d'espace de noms XML suivantes dans la balise \<schema\> :</span><span class="sxs-lookup"><span data-stu-id="721b3-183">To ensure that an XSD file supports the full XSD recommendation, it should contain the following XML namespace declaration in the \<schema\> tag:</span></span>
  
```XML
xmlns:xsd="http://www.w3.org/2001/XMLSchema"
```

<span data-ttu-id="721b3-p120">D'une façon similaire à toutes les déclarations d'espace de noms XML, le préfixe XML (dans ce cas, « xsd ») peut être toute chaîne de préfixe valide. « xsd », « xs » et « '' » (pas de préfixe) sont des préfixes courants que vous pouvez voir en pratique . MSXML signale généralement une erreur à propos de la racine incorrectement définie si la déclaration d'espace de noms est manquante.</span><span class="sxs-lookup"><span data-stu-id="721b3-p120">Similar to all XML namespace declarations, the XML prefix (in this case 'xsd') can be any valid prefix string. Some common prefixes you may see in practice are 'xsd', 'xs', and '' (no prefix). MSXML usually reports an error about the root not being properly defined if this namespace declaration is missing.</span></span>
  
## <a name="importing-and-including-schemas"></a><span data-ttu-id="721b3-187">Importation et inclusion de schémas</span><span class="sxs-lookup"><span data-stu-id="721b3-187">Importing and Including Schemas</span></span>

<span data-ttu-id="721b3-p121">Les schémas XSD sont extensibles et peuvent importer et inclure d'autres schémas. Généralement, vous devez importer un schéma si le schéma spécifié dans l'attribut **targetNamespace** diffère du schéma actuel. Vous devez l'inclure si le schéma spécifié dans l'attribut **targetNamespace** est le même que le schéma actuel.</span><span class="sxs-lookup"><span data-stu-id="721b3-p121">XSD schemas are extensible and can import and include other schemas. Generally, you should import a schema if the schema specified in the **targetNamespace** attribute differs from the current schema. You should include it if the schema specified in the **targetNamespace** attribute is the same as the current schema.</span></span> 
  
<span data-ttu-id="721b3-191">Les sémantiques pour l'importation et l'inclusion de schémas sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="721b3-191">The semantics for importing and including schemas are as follows:</span></span>
  
```XML
<xsd:import namespace = "[anyURI]" schemaLocation = "[anyURI]"/> 
<xsd:include schemaLocation = "[anyURI]"/> 

```

<span data-ttu-id="721b3-p122">Si l'attribut **schemaLocation** est manquant (comme cela arrive avec certains convertisseurs), MSXML déclenche une erreur car il ne peut pas trouver le fichier. Si vous recevez cette erreur, vérifiez également que la ressource ou l'emplacement spécifié dans l'attribut schemaLocation est accessible par les utilisateurs du modèle de formulaire. Des erreurs se produisent évidemment si l'attribut **schemaLocation** référence un serveur ou un répertoire inactif ou inexistant, ou si les utilisateurs n'ont pas les autorisations d'accès. Vérifiez également que tous les schémas importés et inclus sont valides.</span><span class="sxs-lookup"><span data-stu-id="721b3-p122">If the **schemaLocation** attribute is missing (as happens with some converters), then MSXML raises an error because it cannot find the file. If you get this error, also check to make sure that the resource or location specified in the schemaLocation attribute is accessible by users of the form template. Obviously, errors occur if the **schemaLocation** attribute references a server or directory that is down or nonexistent or if users do not have access permissions. Also, be sure to examine all imported and included schemas to make sure they are valid.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="721b3-p123">[!REMARQUE] Les erreurs provoquées par des problèmes liés à l'attribut **schemaLocation** sont problématiques seulement si InfoPath importe d'abord les schémas, c'est-à-dire lorsque vous commencez d'abord par concevoir un formulaire basé sur un schéma existant. Après cela, InfoPath travaille avec des versions mises en cache des fichiers de schéma qui sont stockés dans le modèle de formulaire.</span><span class="sxs-lookup"><span data-stu-id="721b3-p123">Errors caused by problems with the **schemaLocation** attribute are an issue only when InfoPath first imports the schemas; that is, when you first start designing a form based on an existing schema. After that, InfoPath works with cached versions of the schema files that are stored in the form template.</span></span> 
  
<span data-ttu-id="721b3-p124">Un attribut d'espace de noms vide est autorisé lors de l'importation d'un schéma si ce schéma ne spécifie pas un attribut **targetNamespace**. En général, l'espace de noms sur le fichier importé doit correspondre à celui de l'attribut **targetNamespace** spécifié dans le schéma que vous importez.</span><span class="sxs-lookup"><span data-stu-id="721b3-p124">An empty namespace attribute is allowed when importing a schema, if that schema does not specify a **targetNamespace** attribute. In general, the namespace on the import must match the **targetNamespace** specified in the schema that you import.</span></span> 
  
## <a name="nondeterministic-schemas"></a><span data-ttu-id="721b3-200">Schémas non déterministes</span><span class="sxs-lookup"><span data-stu-id="721b3-200">Nondeterministic Schemas</span></span>

<span data-ttu-id="721b3-p125">L'infrastructure MSXML 5.0 dont dépend InfoPath peut détecter et déclencher des erreurs de façon fiable pour vous alerter dans le cas de schémas non déterministes, mais le message d'erreur résultant ne fournit pas de numéro de ligne pour vous indiquer quelle partie du schéma provoque l'erreur. Cette section explique pourquoi il est important que les fichiers de schéma XSD soient déterministes et ce que cela signifie d'être non déterministe. Elle montre également quelques erreurs courantes à éviter.</span><span class="sxs-lookup"><span data-stu-id="721b3-p125">The MSXML 5.0 infrastructure that InfoPath depends upon can reliably detect and raise errors to alert you to nondeterministic schemas, but the resultant error message does not provide a line number to tell you which part of the schema is raising the error. This section discusses why it is important for XSD schema files to be deterministic and what it means to be nondeterministic. It also shows some common errors to avoid.</span></span>
  
<span data-ttu-id="721b3-p126">Les schémas XSD existent pour valider la structure de données et les sémantiques des types du code XML. Pour accomplir cette tâche, le système de validation (dans ce cas, MSXML 5.0) doit mapper des nœuds XML à des déclarations XSD. Sans ce mappage, le système de validation ne peut pas accomplir cette tâche. Si un mappage peut être garanti, le schéma est alors dit déterministe. S'il existe au moins une instance XML qui rend ce mappage impossible, le schéma est dit non déterministe.</span><span class="sxs-lookup"><span data-stu-id="721b3-p126">XSD schemas exist for the purpose of validating XML data structure and type semantics. To accomplish this task, the validating system (in this case, MSXML 5.0) must map XML nodes to XSD declarations. Without this mapping, the validating system cannot accomplish its task. If a mapping can be guaranteed, then the schema is deterministic. If there is a single XML instance that makes this mapping impossible, then the schema is nondeterministic.</span></span>
  
<span data-ttu-id="721b3-209">L'exemple de schéma suivant est non déterministe :</span><span class="sxs-lookup"><span data-stu-id="721b3-209">The following example schema is nondeterministic:</span></span>
  
```XML
<xsd:element name="file_Information"> 
    <xsd:complexType> 
        <xsd:sequence> 
            <xsd:element name="file_name"/> 
            <xsd:choice> 
                <xsd:element name="file_path"/> 
                <xsd:sequence> 
                    <xsd:element name="file_path" minOccurs="0"/> 
                    <xsd:element name="URI"/> 
                </xsd:sequence> 
            </xsd:choice> 
        </xsd:sequence> 
    </xsd:complexType> 
</xsd:element> 

```

<span data-ttu-id="721b3-210">Pour illustrer pourquoi ce segment XSD est non déterministe, supposons que vous avez le fragment XML suivant, que vous voulez valider avec ce schéma :</span><span class="sxs-lookup"><span data-stu-id="721b3-210">To illustrate why this XSD segment is nondeterministic, assume you have the following XML fragment that you want to validate with this schema:</span></span>
  
```XML
<file_Information> 
    <file_name>my_Schema.xsd</file_name> 
    <file_path>c:\xsd</file_path> 
</file_Information> 

```

<span data-ttu-id="721b3-p127">Dans ce fragment XML, il n'apparaît pas clairement si l'élément  *\<file_path\>*  est le nœud requis de la première partie de la déclaration choice ou s'il est le nœud facultatif de la deuxième partie de la déclaration choice. Cette distinction est importante pour les raisons suivantes :</span><span class="sxs-lookup"><span data-stu-id="721b3-p127">In this XML fragment, it is not clear whether the  *\<file_path\>*  element is the required node from the first part of the choice declaration or the optional one from the second part of the choice declaration. This distinction is important for the following reasons:</span></span> 
  
1. <span data-ttu-id="721b3-213">Si le fragment XML est validé par rapport à la première partie de la déclaration choice, le code XML est valide par rapport au premier schéma.</span><span class="sxs-lookup"><span data-stu-id="721b3-213">If the XML fragment is validated against the first part of the choice declaration, then the XML is valid against the schema.</span></span>
    
2. <span data-ttu-id="721b3-214">Si le fragment XML est validé par rapport à la seconde partie de la déclaration choice, le schéma n'est pas valide car le nœud \<URI\> requis est manquant.</span><span class="sxs-lookup"><span data-stu-id="721b3-214">If the XML fragment is validated against the second part of the choice declaration, then the schema is not valid, because the required \<URI\> node is missing.</span></span> 
    
<span data-ttu-id="721b3-p128">Certains systèmes de validation XSD ne déclenchent pas d'erreur de validation par rapport à ce schéma car il existe un chemin d'accès valide. MSXML est plus strict et déclenche une erreur indiquant que le schéma est non déterministe.</span><span class="sxs-lookup"><span data-stu-id="721b3-p128">Some XSD validation systems err toward validating against this schema because there is a valid path. MSXML is stricter and raises an error stating that the schema is nondeterministic.</span></span>
  
<span data-ttu-id="721b3-p129">Quelques autres schémas non déterministes sont présentés ci-dessous. Le premier inclut des éléments facultatifs. Ces situations se produisent souvent avec les convertisseurs XDR vers XSD en raison de différences dans les cardinalités par défaut dans les deux langages de schéma. Le premier cas à considérer est celui d'éléments facultatifs déclarés avec des éléments **xsd:choice** et **xsd:sequence**. Les éléments facultatifs déclarés dans un élément **xsd:sequence** sont généralement validés correctement dès lors que vous n'avez pas plusieurs éléments du même nom, avec seulement des éléments facultatifs entre ceux-ci. Par exemple :</span><span class="sxs-lookup"><span data-stu-id="721b3-p129">What follows are a few more examples of nondeterministic schemas. The first deals with optional elements. These cases often arise from XDR to XSD converters because of differences in the default cardinalities in the two schema languages. The first case to consider is optional elements declared with **xsd:choice** and **xsd:sequence** elements. Optional elements declared in an **xsd:sequence** element usually validate properly, as long as you do not have elements with the same name more than once, with only optional elements in between. For example:</span></span> 
  
```XML
<xsd:element name="container"> 
    <xsd:complexType> 
        <xsd:sequence> 
            <xsd:element ref="aNode" /> 
            <xsd:element ref="anotherNode" minOccurs="0"/> 
            <xsd:element ref="aNode" /> 
        </xsd:sequence> 
    </xsd:complexType> 
</xsd:element> 

```

<span data-ttu-id="721b3-223">Pour comprendre pourquoi ce segment de schéma est non déterministe, supposons que vous avez le fragment XML non valide suivant :</span><span class="sxs-lookup"><span data-stu-id="721b3-223">To understand why this schema segment is nondeterministic, assume you have the following invalid XML fragment:</span></span>
  
```XML
<container> 
    <aNode/> 
    <aNode/> 
    <anotherNode/> 
</container> 

```

<span data-ttu-id="721b3-224">Si vous examinez ce fragment, vous pouvez voir pourquoi il est non valide : il y a deux éléments  `<aNode>` avant l'élément  `<anotherNode>`, alors qu'un seul est autorisé.</span><span class="sxs-lookup"><span data-stu-id="721b3-224">Looking at this fragment, you can see why it is invalid: there are two  `<aNode>` elements before the  `<anotherNode>` element, when only one is allowed.</span></span> 
  
<span data-ttu-id="721b3-225">Supposons maintenant que vous avez l'instance XML suivante à valider :</span><span class="sxs-lookup"><span data-stu-id="721b3-225">Now assume that you have the following XML instance to validate:</span></span>
  
```XML
<container> 
    <aNode/> 
    <aNode/> 
</container> 

```

<span data-ttu-id="721b3-p130">Le problème est de déterminer si cette instance est valide. Avez-vous deux éléments  `<aNode>` alors qu'un seul est autorisé, ou avez-vous un élément  `<aNode>` là où il est autorisé et un autre là où il est autorisé ? Le schéma est non déterministe car il n'y a pas de moyen de connaître la réponse.</span><span class="sxs-lookup"><span data-stu-id="721b3-p130">The challenge is to determine whether this instance is valid. Do you have two  `<aNode>` elements where only one is allowed, or do you have an  `<aNode>` element where it is allowed and another where it is allowed? The schema is nondeterministic because there is no way to know.</span></span> 
  
<span data-ttu-id="721b3-p131">De la même manière, les éléments facultatifs déclarés dans un élément **xsd:choice** sont généralement problématiques. Dans l'exemple simplifié suivant, il n'y a pas moyen de déterminer si le choix s'est produit une fois avec l'élément facultatif ou s'il ne s'est jamais produit du tout.</span><span class="sxs-lookup"><span data-stu-id="721b3-p131">Similarly, optional elements declared in an **xsd:choice** element are usually problematic. In the following simplified example, there is no way to determine whether the choice occurred once with the optional element not being there or whether it never occurred at all.</span></span> 
  
```XML
<xsd:choice> 
    <xsd:element name="node" minOccurs="0"/> 
</xsd:choice> 

```

<span data-ttu-id="721b3-p132">La pratique discutable finale est d'utiliser un élément **xsd:any** sans une définition d'espace de noms, comme dans  `<xsd:any namespace="##other"/>`, après un élément **xsd:sequence**. Cette construction est spécialement gênante lorsqu'elle suit un élément facultatif. Si vous reprenez l'exemple précédent et que vous changez simplement le dernier nœud en un élément **xsd:any**, vous pouvez voir que tous les arguments précédents à propos du non-déterminisme s'appliquent encore, comme suit :</span><span class="sxs-lookup"><span data-stu-id="721b3-p132">The final questionable practice is using an **xsd:any** element without a namespace definition, as in  `<xsd:any namespace="##other"/>` , after an **xsd:sequence** element. This construct is especially troublesome when it follows an optional element. If you revisit the previous example and change just the last node to an **xsd:any** element, you can see that all the previous arguments about nondeterminism still apply, as follows:</span></span> 
  
```XML
<xsd:element name="container"> 
    <xsd:complexType> 
        <xsd:sequence> 
            <xsd:element ref="aNode" /> 
            <xsd:element ref="anotherNode" minOccurs="0"/> 
            <xsd:any />     
        </xsd:sequence> 
    </xsd:complexType> 
</xsd:element> 

```

## <a name="illegal-enumeration-values"></a><span data-ttu-id="721b3-234">Valeurs d'énumération interdites</span><span class="sxs-lookup"><span data-stu-id="721b3-234">Illegal Enumeration Values</span></span>

<span data-ttu-id="721b3-p133">Les schémas XSD n'effectuent généralement aucune validation de type tant que vous n'avez pas validé un document d'instance réel. Une exception à cela est le cas où vous avez une énumération dans votre schéma. Dans ce cas, le schéma valide l'énumération par rapport aux types enumeration pour vérifier qu'ils constituent des valeurs correctes pour les nœuds. Voici deux exemples :</span><span class="sxs-lookup"><span data-stu-id="721b3-p133">XSD schemas typically do not perform any type validation until you validate an actual instance document. An exception to this is when you have an enumeration in your schema. In this case, the schema validates the enumeration values against the enumeration types to ensure they are proper node values. Here are two examples:</span></span>
  
```XML
<xsd:simpleType name="showTimes"> 
    <xsd:restriction base="xsd:time"> 
        <xsd:enumeration value="18:30:00"/> 
        <xsd:enumeration value="20:45:00"/> 
        <xsd:enumeration value="eleven o'clock"/> 
    </xsd:restriction> 
</xsd:simpleType> 

```

<span data-ttu-id="721b3-239">Ce schéma est non valide car "eleven o'clock" n'est pas une valeur valide pour un élément de type **xsd:time**.</span><span class="sxs-lookup"><span data-stu-id="721b3-239">This schema is invalid because "eleven o'clock" is not a valid value for an element of type **xsd:time**.</span></span>
  
<span data-ttu-id="721b3-240">Voici un exemple plus complexe :</span><span class="sxs-lookup"><span data-stu-id="721b3-240">The following is a more complex example:</span></span>
  
```XML
<xsd:simpleType name="concession"> 
    <xsd:restriction base="xsd:NMTOKEN"> 
        <xsd:enumeration value="GummyBears"/> 
        <xsd:enumeration value="SnowCaps"/> 
        <xsd:enumeration value="M&Ms"/> 
    </xsd:restriction> 
</xsd:simpleType> 

```

<span data-ttu-id="721b3-p134">Pour comprendre pourquoi cet exemple est non valide, vous devez comprendre comment le type **xsd:NMTOKEN** est défini. La spécification des types de données W3C définit le type **NMTOKEN** comme suit : « Un jeton de nom (NMTOKEN) est tout ensemble de caractères de nom ».</span><span class="sxs-lookup"><span data-stu-id="721b3-p134">To understand why this example is invalid, you must understand how the type **xsd:NMTOKEN** is defined. The W3C data types specification defines the **NMTOKEN** type as follows: "An NMTOKEN (name token) is any mixture of name characters."</span></span> 
  
<span data-ttu-id="721b3-243">Si vous examinez, vous trouvez que « & » n’êtes pas un caractère de nom valide, et par conséquent, « M & Ms » ne valide pas comme type **NMTOKEN** .</span><span class="sxs-lookup"><span data-stu-id="721b3-243">If you investigate further, you find that '&' is not a valid name character, and therefore "M&Ms" does not validate as an **NMTOKEN** type.</span></span> 
  
## <a name="empty-sequence-or-choice-elements"></a><span data-ttu-id="721b3-244">Éléments sequence ou choice vides</span><span class="sxs-lookup"><span data-stu-id="721b3-244">Empty Sequence or Choice Elements</span></span>

<span data-ttu-id="721b3-245">MSXML déclenche parfois des erreurs à propos de déclarations de schéma contenant des éléments **xsd:choice** ou **xsd:sequence** vides, comme dans l'exemple suivant.</span><span class="sxs-lookup"><span data-stu-id="721b3-245">MSXML sometimes raises errors about schema declarations that contain empty **xsd:choice** or **xsd:sequence** elements, as shown in the following example.</span></span> 
  
```XML
<xsd:element name="emptyContainer"> 
    <xsd:complexType> 
        <xsd:choice /> 
    </xsd:complexType> 
</xsd:element> 

```

<span data-ttu-id="721b3-246">La suppression de la balise  `<xsd:choice />` vide doit résoudre ce problème.</span><span class="sxs-lookup"><span data-stu-id="721b3-246">Removing the empty  `<xsd:choice />` tag should resolve this problem.</span></span> 
  
## <a name="regular-expressions"></a><span data-ttu-id="721b3-247">Expressions régulières</span><span class="sxs-lookup"><span data-stu-id="721b3-247">Regular Expressions</span></span>

<span data-ttu-id="721b3-248">MSXML 5.0 peut avoir des problèmes pour valider des modèles d'expressions régulières lors du chargement.</span><span class="sxs-lookup"><span data-stu-id="721b3-248">MSXML 5.0 can have problems validating regular expression patterns on load.</span></span> <span data-ttu-id="721b3-249">Les expressions régulières peuvent être compliquées, et vous devez être attentif lorsque vous les utilisez.</span><span class="sxs-lookup"><span data-stu-id="721b3-249">Regular expressions can be complicated, and you should be careful when you are using them.</span></span> <span data-ttu-id="721b3-250">Chaque analyseur syntaxique XSD semble avoir des langages flexibles pour les expressions régulières : ils implémentent le langage d'expressions régulières XSD officiel ainsi que des éléments provenant d'autres langages d'expressions régulières.</span><span class="sxs-lookup"><span data-stu-id="721b3-250">Every XSD parser seems to have flexible regular expression languages; that is, they implement the official XSD regular expression language plus elements from other regular expression languages.</span></span> <span data-ttu-id="721b3-251">Si le concepteur de formulaires d'InfoPath a des problèmes pour analyser une expression régulière, les exemples de données générés par InfoPath peuvent être non valides ou ne pas être générées du tout.</span><span class="sxs-lookup"><span data-stu-id="721b3-251">If InfoPath form designer has problems parsing a regular expression, then the sample data InfoPath generates might be invalid or might not be generated at all.</span></span> <span data-ttu-id="721b3-252">Ceci est acceptable lors de la conception, car InfoPath utilise les exemples de données seulement pour la mise en forme.</span><span class="sxs-lookup"><span data-stu-id="721b3-252">This is acceptable at design time, because InfoPath uses only sample data for formatting.</span></span> <span data-ttu-id="721b3-253">Cependant, si vous utilisez une expression régulière qui n'est pas prise en charge par MSXML, InfoPath ne peut pas valider une valeur par rapport à cette expression lorsqu'un utilisateur remplit un formulaire.</span><span class="sxs-lookup"><span data-stu-id="721b3-253">However, if you use a regular expression that MSXML does not support, then InfoPath cannot validate a value against it when a user is filling out a form.</span></span> <span data-ttu-id="721b3-254">[XML Schema Part 0 : Primer Second Edition](http://www.w3.org/TR/xmlschema-0/)décrit ce qui est pris en charge dans les expressions régulières XSD.</span><span class="sxs-lookup"><span data-stu-id="721b3-254">[XML Schema Part 0: Primer Second Edition](http://www.w3.org/TR/xmlschema-0/)describes what is supported in XSD regular expressions.</span></span> <span data-ttu-id="721b3-255">Pour plus d’informations sur les expressions régulières XSD et les expressions régulières de niveau 1 Unicode, voir [Expressions régulières Unicode](http://www.unicode.org/reports/tr18/) .</span><span class="sxs-lookup"><span data-stu-id="721b3-255">For more information about XSD regular expressions and Unicode level 1 regular expressions, see [Unicode Regular Expressions](http://www.unicode.org/reports/tr18/) .</span></span> 
  
## <a name="targetnamespace-attribute-issues"></a><span data-ttu-id="721b3-256">Problèmes liés à l'attribut targetNamespace</span><span class="sxs-lookup"><span data-stu-id="721b3-256">targetNamespace Attribute Issues</span></span>

<span data-ttu-id="721b3-p136">XSD est intéressant en ceci que, par défaut, l'attribut **targetNamespace** référence seulement les déclarations du plus haut niveau, bien qu'il soit possible de définir  `attributeFormDefault=qualified` et  `elementFormDefault=qualified` pour remplacer ce comportement par défaut. Par exemple, supposons que vous avez le code XSD suivant.</span><span class="sxs-lookup"><span data-stu-id="721b3-p136">XSD is interesting in that, by default, the **targetNamespace** attribute refers to only the top-level declarations, although you can set  `attributeFormDefault=qualified` and  `elementFormDefault=qualified` to override this default behavior. As an example, assume that you have the following XSD.</span></span> 
  
```XML
<xsd:schema xmlns:xsd="http://www.w3.org/2001/XMLSchema" targetNamespace="http://ns" > 
    <xsd:element name="root"> 
        <xsd:complexType> 
            <xsd:sequence> 
                <xsd:element name="local"/> 
            </xsd:sequence> 
        </xsd:complexType> 
    </xsd:element> 
</xsd:schema> 

```

<span data-ttu-id="721b3-259">Et supposons que votre document d'instance XML ressemble à l'exemple suivant.</span><span class="sxs-lookup"><span data-stu-id="721b3-259">And that, your XML instance document resembles the following example.</span></span>
  
```XML
<ns:root xmlns:ns="http://ns"> 
    <local/> 
</ns:root> 

```

<span data-ttu-id="721b3-p137">Les définitions locales ne requièrent pas d'espace de noms cible car la qualification est désactivée par défaut. Cependant, si vous changez votre définition locale en globale, votre référence doit être qualifiée avec le préfixe d'espace de noms. Par exemple, le schéma suivant est non valide.</span><span class="sxs-lookup"><span data-stu-id="721b3-p137">Local definitions do not require the target namespace because qualification is turned off by default. However, if you change your local definition to be global, then your reference must be qualified with the namespace prefix. For example, the following schema is invalid.</span></span>
  
```XML
<xsd:schema xmlns:xsd="http://www.w3.org/2001/XMLSchema" targetNamespace="http://ns" > 
    <xsd:element name="root"> 
        <xsd:complexType> 
            <xsd:sequence> 
                <xsd:element ref="global"/> 
            </xsd:sequence> 
        </xsd:complexType> 
    </xsd:element> 
 
    <xsd:element name="global"/> 
</xsd:schema> 

```

<span data-ttu-id="721b3-p138">Ce schéma est non valide car "global" est dans l'espace de noms "http://ns". L'élément simple ref="global" n'est pas reconnu car l'espace de noms par défaut n'est pas "http://ns". Pour résoudre cela, vous devez ajouter un préfixe pour l'espace de noms cible et utiliser ceci pour toutes les références globales et les utilisations des types. Le schéma corrigé est similaire à celui-ci.</span><span class="sxs-lookup"><span data-stu-id="721b3-p138">This schema is invalid because "global" is in the namespace "http://ns". The simple ref="global" is not recognized because the default namespace is not "http://ns". To fix this, you must add a prefix for the target namespace and use that for all global references and type uses. The corrected schema looks like the following.</span></span>
  
```XML
<xsd:schema xmlns:xsd="http://www.w3.org/2001/XMLSchema"  
    xmlns:ns="http://ns" targetNamespace="http://ns" > 
    <xsd:element name="root"> 
        <xsd:complexType> 
            <xsd:sequence> 
                <xsd:element ref="ns:global"/> 
            </xsd:sequence> 
        </xsd:complexType> 
    </xsd:element> 
 
    <xsd:element name="global"/> 
</xsd:schema> 

```

<span data-ttu-id="721b3-267">Si l'attribut **targetNamespace** est spécifié dans votre schéma, vérifiez que toutes les références globales sont qualifiées avec le préfixe d'espace de noms correct.</span><span class="sxs-lookup"><span data-stu-id="721b3-267">If your schema has the **targetNamespace** attribute specified, ensure that all global references are qualified with the correct namespace prefix.</span></span> 
  
## <a name="xml-processing-instruction-encoding-unicode-vs-ansii"></a><span data-ttu-id="721b3-268">Codage des instructions de traitement XML (Unicode ou ANSII)</span><span class="sxs-lookup"><span data-stu-id="721b3-268">XML Processing Instruction Encoding (Unicode vs. ANSII)</span></span>

<span data-ttu-id="721b3-p139">XML prend en charge seulement les jeux de caractères Unicode. Par conséquent, vous pouvez perdre des informations si vous enregistrez des fichiers qui utilisent des caractères ANSII. L'enregistrement des fichiers au format UTF-16 peut néanmoins être excessif pour votre utilisation spécifique. Pour réduire le coût d'implémentation d'un lecteur XML, le créateur de code XML doit indiquer le codage qu'il utilise dans l'instruction de traitement XML du plus haut niveau. Vous reconnaissez sans doute l'instruction de traitement suivante.</span><span class="sxs-lookup"><span data-stu-id="721b3-p139">XML supports only Unicode character sets. Therefore, you may lose information if you save files that use ANSII characters. However, saving files as UTF-16 may be excessive for your particular use. To reduce the implementation cost of an XML reader, the XML author must state which encoding they are using in the top-level XML processing instruction. You may recognize the following processing instruction.</span></span>
  
```XML
xml version="1.0" encoding="UTF-8"
```

<span data-ttu-id="721b3-p140">Cette balise d'instruction de traitement spécifie que le codage du fichier est UTF-8. Vous devez vérifier que le codage du fichier est le même que celui qui est indiqué dans cette balise. Vous pouvez déterminer le codage en examinant les octets du fichier et en recherchant les indicateurs Unicode d'ordre des octets. Il existe cependant un moyen plus facile. Si vous avez des problèmes pour ouvrir un schéma XSD, spécifiez un codage « UTF-8 », ouvrez-le dans un éditeur de texte tel que le Bloc-notes, puis enregistrez le fichier avec le codage UTF-8 (le Bloc-notes a une liste déroulante **Codage** dans la boîte de dialogue **Enregistrer sous**). Si vous avez encore des problèmes pour ouvrir le fichier, c'est que ce n'est pas un problème de codage.</span><span class="sxs-lookup"><span data-stu-id="721b3-p140">This processing instruction tag specifies that the encoding of the file is UTF-8. You must ensure that the file encoding is the same as the encoding stated in the processing instruction tag. You can determine the encoding by looking at the bytes of the file and looking for the Unicode byte order marks. But there is an easier way. If you have problems opening an XSD schema, specify the encoding as "UTF-8", open it in a text editor such as Notepad, and then save the file by using UTF-8 encoding (Notepad provides the **Encoding** drop-down list in the **Save As** dialog box). If you still have problems opening the file, it is not an encoding issue.</span></span> 
  
## <a name="maxoccurs-attribute-inside-the-xsdall-element"></a><span data-ttu-id="721b3-280">Attribut maxOccurs à l'intérieur d'un élément xsd:all</span><span class="sxs-lookup"><span data-stu-id="721b3-280">maxOccurs Attribute Inside the xsd:all Element</span></span>

<span data-ttu-id="721b3-p141">En raison de la façon dont le non-déterminisme est défini dans la recommandation pour les schémas XML, la seule valeur valide pour l'attribut **maxOccurs** d'un élément **xsd:element** à l'intérieur d'un élément **xsd:all** est 1. Par exemple, le code suivant est valide.</span><span class="sxs-lookup"><span data-stu-id="721b3-p141">Due to the way nondeterminism is defined in the XML Schema recommendation, the only valid value for the **maxOccurs** attribute of an **xsd:element** element inside an **xsd:all** element is 1. For example, the following is valid.</span></span> 
  
```XML
<xsd:all> 
    <xsd:element name="x" minOccurs="0"/> 
    <xsd:element name="docs" minOccurs="0"/> 
</xsd:all> 

```

<span data-ttu-id="721b3-283">Par contre, cet exemple n'est pas valide.</span><span class="sxs-lookup"><span data-stu-id="721b3-283">However, this example is not valid.</span></span>
  
```XML
<xsd:all>     
    <xsd:element name="x" minOccurs="0" maxOccurs="unbounded"/> 
    <xsd:element name="docs" minOccurs="0" maxOccurs="unbounded"/> 
</xsd:all> 

```

<span data-ttu-id="721b3-p142">Cet exemple est non valide car le système de validation ne peut pas déterminer si deux occurrences de  `<x/>` correspondent à la déclaration unique, ou à la déclaration et à une autre définition non valide. Dans les mêmes lignes, vous ne pouvez pas avoir deux éléments du même nom dans une balise  `<xsd:all>`.</span><span class="sxs-lookup"><span data-stu-id="721b3-p142">This example is invalid because the validation system cannot determine whether two occurrences of  `<x/>` map to the single declaration or to the declaration and another invalid definition. Along the same lines, you cannot have two elements of the same name in an  `<xsd:all>` tag.</span></span> 
  
<span data-ttu-id="721b3-p143">Cet exemple est également intéressant car il vous permet d'avoir un nombre quelconque de nœuds  `<x/>` et  `<docs/>` à l'intérieur d'un élément conteneur, dans un ordre quelconque. Bien que cette construction ne soit pas valide, il existe une solution de contournement. En utilisant l'élément **xsd:choice**, vous pouvez obtenir le même résultat, comme le montre l'exemple suivant.</span><span class="sxs-lookup"><span data-stu-id="721b3-p143">This example is also interesting because it allows you to have any number of  `<x/>` and  `<docs/>` nodes inside a containing element in any order. Although this construct is invalid, there is a workaround. By using the **xsd:choice** element, you can achieve the same result, as demonstrated in the following example.</span></span> 
  
```XML
<xsd:choice minOccurs="0" maxOccurs="unbounded"> 
    <xsd:element name="x" /> 
    <xsd:element name="docs" /> 
</xsd:choice> 

```

## <a name="how-to-edit-or-author-an-xsd-for-infopath"></a><span data-ttu-id="721b3-289">Modification ou création d'un schéma XSD pour InfoPath</span><span class="sxs-lookup"><span data-stu-id="721b3-289">How to Edit or Author an XSD for InfoPath</span></span>

<span data-ttu-id="721b3-290">Les deux exemples des sections suivantes montrent comment modifier ou créer un schéma pour produire des résultats spécifiques dans InfoPath.</span><span class="sxs-lookup"><span data-stu-id="721b3-290">The two examples in the following sections show how to edit or author a schema to produce specific results in InfoPath.</span></span>
  
## <a name="allowing-user-defined-elements-to-be-inserted-in-the-fields-task-pane"></a><span data-ttu-id="721b3-291">Possibilité d'insérer des éléments définis par l'utilisateur dans le volet Office Champs</span><span class="sxs-lookup"><span data-stu-id="721b3-291">Allowing User-defined Elements to Be Inserted in the Fields Task Pane</span></span>

<span data-ttu-id="721b3-p144">Pour permettre à des éléments définis par l'utilisateur d'apparaître sous un élément parent dans le volet Office **Champs**, vous devez insérer un élément **xsd:any** sous l'élément parent. Pour permettre à des éléments définis par l'utilisateur d'être insérés à l'intérieur de  `<your_node_name>`, la déclaration XSD doit être similaire à ce qui suit.</span><span class="sxs-lookup"><span data-stu-id="721b3-p144">To allow user-defined elements to appear under a parent element in the **Fields** task pane, you must insert an **xsd:any** element under the parent element. To allow user-defined elements to be inserted inside  `<your_node_name>` , the XSD declaration should resemble the following.</span></span> 
  
```XML
<xsd:element name="your_node_name"> 
    <xsd:complexType> 
        <xsd:sequence> 
            <xsd:any namespace="##any | ##other"  
                minOccurs="0" maxOccurs="unbounded"/> 
        </xsd:sequence> 
    </xsd:complexType> 
</xsd:element> 

```

<span data-ttu-id="721b3-294">Si vous voulez aussi autoriser les attributs définis par l'utilisateur, vous devez ajouter  `<xsd:anyAttribute namespace="##any | ##other"/>` à la déclaration element.</span><span class="sxs-lookup"><span data-stu-id="721b3-294">If you also want to allow user-defined attributes, then you must add  `<xsd:anyAttribute namespace="##any | ##other"/>` to the element declaration.</span></span> 
  
## <a name="allowing-rich-text-elements-to-be-bound-in-infopath-design-and-edit-modes"></a><span data-ttu-id="721b3-295">Possibilité de liaison d'éléments de texte enrichi dans les modes Création et Édition</span><span class="sxs-lookup"><span data-stu-id="721b3-295">Allowing Rich Text Elements to be Bound in InfoPath Design and Edit Modes</span></span>

<span data-ttu-id="721b3-296">Si vous voulez déclarer un élément qui peut être lié à un contrôle **Rich Text Box**, il doit avoir la forme suivante, qui inclut l'élément **xsd:any**, qui a un attribut namespace défini à "http://www.w3.org/1999/xhtml", comme le montre l'exemple suivant.</span><span class="sxs-lookup"><span data-stu-id="721b3-296">If you want to declare an element that can be bound to a **Rich Text Box** control, then it should have the following form, which includes the **xsd:any** element that has a namespace attribute set to "http://www.w3.org/1999/xhtml" as shown in the following example.</span></span> 
  
```XML
<xsd:element name="your_node_name"> 
    <xsd:complexType mixed="true"> 
        <xsd:sequence> 
            <xsd:any namespace="http://www.w3.org/1999/xhtml"  
                minOccurs="0" maxOccurs="unbounded"/> 
        </xsd:sequence> 
    </xsd:complexType> 
</xsd:element> 

```

## <a name="conclusion"></a><span data-ttu-id="721b3-297">Conclusion</span><span class="sxs-lookup"><span data-stu-id="721b3-297">Conclusion</span></span>

<span data-ttu-id="721b3-p145">En tirant profit de la prise en charge par InfoPath de la conception de solutions de formulaires XML basées sur des fichiers de schéma XML (.xsd) créés en externe, vous pouvez créer un modèle de formulaire qui fonctionne avec un schéma standard ou avec un schéma créé par votre entreprise ou votre organisation. À l'aide des informations contenues dans cet article, vous pouvez créer des fichiers de schéma XSD qui sont compatibles avec InfoPath, et vous pouvez résoudre des problèmes courants que vous êtes susceptible de rencontrer lorsque vous chargez dans l'environnement de conception InfoPath des fichiers XSD créés en externe.</span><span class="sxs-lookup"><span data-stu-id="721b3-p145">By taking advantage of InfoPath support for designing XML form solutions that are based on externally authored XML Schema (.xsd) files, you can create a form template that works with an industry-standard schema or custom schema created by your company or organization. By using the information in this article, you can create custom XSD schema files that are compatible with InfoPath, and you can troubleshoot common issues that you may encounter when you load externally authored XSD files into the InfoPath design environment.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="721b3-300">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="721b3-300">See also</span></span>

- [<span data-ttu-id="721b3-301">W3C XML Schema (éventuellement en anglais)</span><span class="sxs-lookup"><span data-stu-id="721b3-301">W3C XML Schema</span></span>](http://www.w3.org/XML/Schema)
- [<span data-ttu-id="721b3-302">W3C XML Schema Primer (éventuellement en anglais)</span><span class="sxs-lookup"><span data-stu-id="721b3-302">W3C XML Schema Primer</span></span>](http://www.w3.org/TR/xmlschema-0/)
- [<span data-ttu-id="721b3-303">W3C XML Schema Structures Reference (éventuellement en anglais)</span><span class="sxs-lookup"><span data-stu-id="721b3-303">W3C XML Schema Structures Reference</span></span>](http://www.xml.com/pub/a/2000/11/29/schemas/structuresref.mdl)
- [<span data-ttu-id="721b3-304">W3C XML Schema Datatypes Reference (éventuellement en anglais)</span><span class="sxs-lookup"><span data-stu-id="721b3-304">W3C XML Schema Datatypes Reference</span></span>](http://www.xml.com/pub/a/2000/11/29/schemas/dataref.mdl)
- [<span data-ttu-id="721b3-305">XML Schema Tutorial (éventuellement en anglais)</span><span class="sxs-lookup"><span data-stu-id="721b3-305">XML Schema Tutorial</span></span>](http://www.w3schools.com/schema/default.asp)
- [<span data-ttu-id="721b3-306">Centre d'accès aux données et stockage (éventuellement en anglais)</span><span class="sxs-lookup"><span data-stu-id="721b3-306">XML Developer Center</span></span>](http://msdn.microsoft.com/en-us/xml/default.aspx)

