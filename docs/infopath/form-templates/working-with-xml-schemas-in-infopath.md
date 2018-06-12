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
# <a name="working-with-xml-schemas-in-infopath"></a>Utilisation des schémas XML dans InfoPath

Un modèle de formulaire que vous créez avec Microsoft InfoPath utilise un schéma XML (XSD) pour effectuer une validation de la structure et des données du code XML qui est en entrée, en modification et en sortie d'un formulaire InfoPath. Chaque modèle de formulaire créé dans le concepteur de formulaires InfoPath contient au moins un fichier de schéma XSD (.xsd) qui est utilisé pour la validation lors de l'exécution.
  
> [!NOTE]
> [!REMARQUE] Les informations contenues dans cette rubrique s'appliquent aux modèles de formulaire conçus pour être utilisés dans l'éditeur d'InfoPath. Les modèles de formulaire compatibles avec un navigateur ont des conditions requises plus strictes quant au schéma XSD. Pour plus d'informations, voir la documentation disponible sur MSDN sur les schémas XML dans les modèles de formulaire compatibles avec un navigateur. 
  
## <a name="using-externally-authored-xml-schemas"></a>Utilisation de schémas XML créés en externe

Pour charger un fichier de schéma XSD qui a été créé en dehors d'InfoPath, procédez selon les étapes suivantes.
  
### <a name="to-create-a-form-template-based-on-an-external-schema"></a>Pour créer un modèle de formulaire basé sur un schéma externe

1. Dans Backstage, cliquez sur **Nouveau**, cliquez sur **Fichier ou schéma XML** sous **Modèles de formulaires avancés**, puis cliquez sur **Modifier ce formulaire**.
    
2. Dans l' **Assistant Source de données**, spécifiez le fichier de schéma XSD que vous voulez utiliser, puis cliquez sur **Suivant** et continuez avec les pages suivantes de l'Assistant. 
    
## <a name="unsupported-xsd-constructs"></a>Constructions XSD non prises en charge

Les sections suivantes décrivent les constructions XSD qu'InfoPath ne peut pas gérer lors de l'exécution. Évitez ces constructions lors de la création d'un modèle de formulaire dans le concepteur de formulaires InfoPath.
  
## <a name="entity-and-entities-types"></a>Types ENTITY et ENTITIES

Les types **ENTITY** et **ENTITIES** requièrent une définition de type de document (DTD) pour la validation, ce qu'InfoPath ne prend pas en charge. InfoPath ne vous permet pas de concevoir un modèle de formulaire basé sur un tel schéma et affiche un message d'erreur recommandant de remplacer le type **ENTITY** par le type **NCName** dont **ENTITY** est dérivé. 
  
> [!NOTE]
>  [!REMARQUE]  Si vous créez manuellement un modèle de formulaire InfoPath en dehors du mode Création et qu'il utilise un schéma XSD incluant les types **ENTITY** et **ENTITIES**, le modèle de formulaire peut éventuellement fonctionner à l'exécution si le fichier Template.xml contient la DTD requise pour ces types. 
  
## <a name="required-xsdany-element"></a>Élément xsd:any requis

Une occurrence d'un élément générique **xsd:any**, c'est-à-dire une occurrence d'un élément **xsd:any** avec une valeur pour l'attribut **minOccurs** supérieure à zéro (paramètre « xsd:any » requis), empêche InfoPath de créer de façon déterministe une instance valide de fragment de schéma. InfoPath doit pouvoir créer une instance valide lors de la génération d'un formulaire qui utilise ce fragment de schéma. Dans le cadre de l'exécution de l' **Assistant Source de données**, les schémas avec des éléments **xsd:any** requis vous obligent à choisir l'élément de schéma que vous voulez utiliser à la place de l'élément **xsd:any** requis. 
  
## <a name="elements-with-an-abstract-complex-type"></a>Éléments avec un type complexe abstrait

Le mode Création d'InfoPath prend en charge la conception d'un modèle de formulaire basé sur des schémas utilisant des types complexes abstraits. Par exemple, si un élément nommé  `shippingAddress` a un type complexe abstrait nommé  `address` qui a deux dérivations,  `USAddress` et  `CanadianAddress`, InfoPath traite les instances de  `shippingAddress` comme un choix entre  `shippingAddress` avec le type  `USAddress` et  `shippingAddress` avec le type  `CanadianAddress`. Dans cet exemple, si les schémas fournis ne contiennent pas de types qui dérivent de cette adresse, InfoPath demande un schéma supplémentaire qui répond à cette condition requise. 
  
## <a name="xsd-constructs-with-reduced-functionality"></a>Constructions XSD avec une fonctionnalité réduite

Les sections suivantes décrivent des constructions XSD qui ont une fonctionnalité réduite lorsqu'ils sont utilisés pour créer un modèle de formulaire dans le concepteur de formulaires InfoPath.
  
## <a name="substitution-groups"></a>Groupes de substitution

Tous les membres du groupe de substitution apparaissent dans le volet Office **Champs**. InfoPath représente les possibilités de substitution comme un choix de tous les groupes de substitution (y compris l'élément de définition s'il n'est pas abstrait). S'il n'existe pas de groupes de substitution pour un élément abstrait, InfoPath vous invite à fournir un schéma contenant au moins un élément qui est un groupe de substitution. 
  
## <a name="unbounded-choice-elements"></a>Éléments choice non liés

Le fragment de schéma suivant montre un élément choice non lié :
  
```XML
<xsd:choice maxOccurs="unbounded"> 
    <xsd:element name="my_element_1"/> 
    <xsd:element name="my_element_2"/> 
</xsd:choice> 

```

InfoPath affiche les éléments choice extensibles en tant que choix extensibles dans le volet Office **Champs**. Il existe un contrôle **Groupe de choix extensible**, que vous pouvez utiliser pour représenter la liste hétérogène définie par l'élément choice extensible dans le schéma XSD. 
  
## <a name="repeating-sequence"></a>Séquence extensible

Le fragment de schéma suivant montre une séquence extensible :
  
```XML
<xsd:sequence maxOccurs="unbounded"> 
    <xsd:element name="my_element_1"/> 
    <xsd:element name="my_element_2" minOccurs="0"/> 
</xsd:sequence> 

```

Tant que la séquence extensible contient un élément requis, InfoPath charge le schéma XSD sans le modifier et vous permet de lier les contrôles de la section extensible à la séquence extensible.
  
## <a name="choice-of-model-groups"></a>Choix de groupes de modèles

Le fragment de schéma suivant montre l'élément choice contenant plusieurs groupes de modèles :
  
```XML
<xsd:choice> 
    <xsd:element name="my_element_1"/> 
    <xsd:sequence> 
        <xsd:element name="my_element_2"/> 
        <xsd:element name="my_element_3"/> 
    </xsd:sequence> 
</xsd:choice> 

```

Le mode Création d'InfoPath prend en charge de telles constructions XSD sans requérir de modifications par le concepteur du formulaire. Comme InfoPath ne modifie pas la signification du schéma, il simplifie la construction choice ci-dessus en un choix unique réduit équivalent dans le volet Office **Champs**. 
  
## <a name="optional-sibling-with-same-qualified-name"></a>Frère facultatif avec le même nom qualifié

Le fragment de schéma suivant montre un frère facultatif avec le même nom qualifié (`QName`) :
  
```xml
<xsd:sequence> 
    <xsd:element name="my_element_1" minOccurs="0"/> 
    <xsd:element name="my_element_2"/> 
            <xsd:element name="my_element_1"/> 
</xsd:sequence> 

```

Les expressions **XPath** pour ces nœuds peuvent être complexes car chaque instance XML potentielle doit être prise en compte dans le concepteur de formulaires d'InfoPath. InfoPath n'expose pas les composants du schéma pour lesquels il peut avoir rencontré des difficultés lors de la création des liaisons **XPath** correctes. Des avertissements apparaissent à propos des parties du schéma qui sont ignorées. 
  
## <a name="xsd-constructs-with-special-meaning-in-infopath"></a>Constructions XSD avec une signification spéciale dans InfoPath

Les sections suivantes décrivent des constructions XSD qui ont une signification spéciale lorsqu'elles sont utilisées dans la création d'un modèle de formulaire en mode Création. Ces sections décrivent comment vous pouvez utiliser les constructions dans votre schéma pour permettre certains comportements.
  
## <a name="adding-new-element-fields-and-groups-with-the-fields-task-pane"></a>Ajout de nouveaux champs et groupes d'éléments avec le volet Office Champs

Vous pouvez construire votre schéma de façon à pouvoir utiliser le volet Office **Champs** pour ajouter de nouveaux champs et groupes d'éléments à un élément lors de la conception. Pour cela, vous déclarez un élément dans votre schéma avec un élément **xsd:any** facultatif non lié, qui spécifie l'attribut namespace avec la valeur générique **##any**. Ensuite, en mode Création, vous pouvez utiliser le volet Office **Champs** pour ajouter de nouveaux champs et groupes d'éléments à cet élément. Par exemple, vous pouvez ajouter un nouveau contenu à l'élément suivant : 
  
```XML
<xsd:element name="open"> 
    <xsd:complexType> 
         <xsd:sequence> 
             <xsd:any minOccurs="0" maxOccurs="unbounded" namespace="##any"processContents="lax"/> 
         </xsd:sequence> 
    </xsd:complexType> 
</xsd:element> 

```

## <a name="adding-new-attribute-fields-with-the-fields-task-pane"></a>Ajout de nouveaux champs d'attribut avec le volet Office Champs

De la même façon que dans le cas d'un élément, vous pouvez déclarer un attribut avec un élément **anyAttribute** dont l'attribut namespace est spécifié avec la valeur générique **##any**. Lors de la conception, vous pouvez utiliser le volet Office **Champs** pour ajouter un nouveau contenu à cet attribut du schéma. 
  
```XML
<xsd:element name="open"> 
    <xsd:complexType> 
        <xsd:anyAttribute namespace="##any" processContents="lax"/> 
    </xsd:complexType> 
</xsd:element> 

```

## <a name="storing-xml-signatures-in-the-data-source"></a>Stockage de signatures XML dans la source de données

Pour permettre aux utilisateurs de signer numériquement un formulaire lors de l'exécution, le schéma de la source de données doit déclarer un élément nommé « signature » pour stocker les informations des signatures numériques XML qui sont créées lorsqu'un utilisateur signe le formulaire. Vous effectuez cette déclaration à l'aide de l'élément **xsd:any** avec l'attribut namespace spécifié en tant qu'espace de noms des signatures XML avec un caractère générique, comme suit : "http://www.w3c.org/2000/09/xmldsig#" 
  
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

## <a name="binding-a-field-to-a-rich-text-box-control"></a>Liaison d'un champ avec un contrôle de zone de texte enrichi

 Les contrôles **Zone de texte enrichi** d'InfoPath génèrent du code XHTML générique ; par conséquent, votre schéma doit spécifier qu'un nombre quelconque de textes et de nœuds XHTML est valide dans le code XML de l'instance du formulaire. Vous pouvez effectuer cette spécification avec la construction XSD suivante : 
  
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
> [!REMARQUE] InfoPath ne modifie jamais le contenu du fichier de schéma (.xsd), mais il peut déduire de façon logique un sous-ensemble de celui-ci à des fins de conception. Le fichier de schéma est toujours laissé intact dans le modèle de formulaire lors de la conception et lors de l'exécution. 
  
## <a name="debugging-common-xsd-errors"></a>Débogage des erreurs XSD courantes

Si vous chargez des fichiers XSD créés en externe pour créer des modèles de formulaire dans le concepteur de formulaires d'InfoPath, vous êtes susceptibles de recevoir deux types de messages d'erreur : des messages d'erreur MSXML ou des messages d'erreur InfoPath. Les messages d'erreur MSXML apparaissent dans la section **Détails** d'une boîte de dialogue de message d'erreur InfoPath, et ils commencent toujours par une référence au nom ou au chemin d'accès du fichier de schéma qui a déclenché l'erreur. Certaines constructions de schéma XSD valides ne sont pas prises en charge par InfoPath ; celles-ci sont présentées dans la section Constructions XSD non prises en charge. Les sections suivantes décrivent certaines erreurs courantes qui provoquent l'échec du chargement correct de schémas dans InfoPath. 
  
## <a name="the-xsd-namespace-declaration"></a>La déclaration d'espace de noms XSD

De façon similaire à tous les standards W3C, les schémas XML (XSD) ont fait l'objet d'un long processus de révision avant de devenir une recommandation. Il a existé de nombreuses versions de travail et par conséquent, de nombreux fichiers XSD ont été écrits sur la base de ces standards en cours d'évolution. Pendant ce processus, Microsoft a créé un langage de schéma propriétaire appelé XDR (XML-Data Reduced), qui a été inclus dans MSXML 3.0. À partir de MSXML 4.0, Microsoft XML Core Services prend en charge la totalité de la recommandation de XSD. De nombreux programmes de création de schémas n'ont pas attendu que XSD devienne une recommandation complète. Les versions antérieures de ces programmes sont susceptibles de produire des fichiers XSD obsolètes, que l'infrastructure MSXML 5.0, dont dépend InfoPath, ne prend pas en charge.
  
Pour garantir qu'un fichier XSD prend en charge la recommandation XSD complète, il doit contenir la déclaration d'espace de noms XML suivantes dans la balise \<schema\> :
  
```XML
xmlns:xsd="http://www.w3.org/2001/XMLSchema"
```

D'une façon similaire à toutes les déclarations d'espace de noms XML, le préfixe XML (dans ce cas, « xsd ») peut être toute chaîne de préfixe valide. « xsd », « xs » et « '' » (pas de préfixe) sont des préfixes courants que vous pouvez voir en pratique . MSXML signale généralement une erreur à propos de la racine incorrectement définie si la déclaration d'espace de noms est manquante.
  
## <a name="importing-and-including-schemas"></a>Importation et inclusion de schémas

Les schémas XSD sont extensibles et peuvent importer et inclure d'autres schémas. Généralement, vous devez importer un schéma si le schéma spécifié dans l'attribut **targetNamespace** diffère du schéma actuel. Vous devez l'inclure si le schéma spécifié dans l'attribut **targetNamespace** est le même que le schéma actuel. 
  
Les sémantiques pour l'importation et l'inclusion de schémas sont les suivantes :
  
```XML
<xsd:import namespace = "[anyURI]" schemaLocation = "[anyURI]"/> 
<xsd:include schemaLocation = "[anyURI]"/> 

```

Si l'attribut **schemaLocation** est manquant (comme cela arrive avec certains convertisseurs), MSXML déclenche une erreur car il ne peut pas trouver le fichier. Si vous recevez cette erreur, vérifiez également que la ressource ou l'emplacement spécifié dans l'attribut schemaLocation est accessible par les utilisateurs du modèle de formulaire. Des erreurs se produisent évidemment si l'attribut **schemaLocation** référence un serveur ou un répertoire inactif ou inexistant, ou si les utilisateurs n'ont pas les autorisations d'accès. Vérifiez également que tous les schémas importés et inclus sont valides. 
  
> [!NOTE]
> [!REMARQUE] Les erreurs provoquées par des problèmes liés à l'attribut **schemaLocation** sont problématiques seulement si InfoPath importe d'abord les schémas, c'est-à-dire lorsque vous commencez d'abord par concevoir un formulaire basé sur un schéma existant. Après cela, InfoPath travaille avec des versions mises en cache des fichiers de schéma qui sont stockés dans le modèle de formulaire. 
  
Un attribut d'espace de noms vide est autorisé lors de l'importation d'un schéma si ce schéma ne spécifie pas un attribut **targetNamespace**. En général, l'espace de noms sur le fichier importé doit correspondre à celui de l'attribut **targetNamespace** spécifié dans le schéma que vous importez. 
  
## <a name="nondeterministic-schemas"></a>Schémas non déterministes

L'infrastructure MSXML 5.0 dont dépend InfoPath peut détecter et déclencher des erreurs de façon fiable pour vous alerter dans le cas de schémas non déterministes, mais le message d'erreur résultant ne fournit pas de numéro de ligne pour vous indiquer quelle partie du schéma provoque l'erreur. Cette section explique pourquoi il est important que les fichiers de schéma XSD soient déterministes et ce que cela signifie d'être non déterministe. Elle montre également quelques erreurs courantes à éviter.
  
Les schémas XSD existent pour valider la structure de données et les sémantiques des types du code XML. Pour accomplir cette tâche, le système de validation (dans ce cas, MSXML 5.0) doit mapper des nœuds XML à des déclarations XSD. Sans ce mappage, le système de validation ne peut pas accomplir cette tâche. Si un mappage peut être garanti, le schéma est alors dit déterministe. S'il existe au moins une instance XML qui rend ce mappage impossible, le schéma est dit non déterministe.
  
L'exemple de schéma suivant est non déterministe :
  
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

Pour illustrer pourquoi ce segment XSD est non déterministe, supposons que vous avez le fragment XML suivant, que vous voulez valider avec ce schéma :
  
```XML
<file_Information> 
    <file_name>my_Schema.xsd</file_name> 
    <file_path>c:\xsd</file_path> 
</file_Information> 

```

Dans ce fragment XML, il n'apparaît pas clairement si l'élément  *\<file_path\>*  est le nœud requis de la première partie de la déclaration choice ou s'il est le nœud facultatif de la deuxième partie de la déclaration choice. Cette distinction est importante pour les raisons suivantes : 
  
1. Si le fragment XML est validé par rapport à la première partie de la déclaration choice, le code XML est valide par rapport au premier schéma.
    
2. Si le fragment XML est validé par rapport à la seconde partie de la déclaration choice, le schéma n'est pas valide car le nœud \<URI\> requis est manquant. 
    
Certains systèmes de validation XSD ne déclenchent pas d'erreur de validation par rapport à ce schéma car il existe un chemin d'accès valide. MSXML est plus strict et déclenche une erreur indiquant que le schéma est non déterministe.
  
Quelques autres schémas non déterministes sont présentés ci-dessous. Le premier inclut des éléments facultatifs. Ces situations se produisent souvent avec les convertisseurs XDR vers XSD en raison de différences dans les cardinalités par défaut dans les deux langages de schéma. Le premier cas à considérer est celui d'éléments facultatifs déclarés avec des éléments **xsd:choice** et **xsd:sequence**. Les éléments facultatifs déclarés dans un élément **xsd:sequence** sont généralement validés correctement dès lors que vous n'avez pas plusieurs éléments du même nom, avec seulement des éléments facultatifs entre ceux-ci. Par exemple : 
  
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

Pour comprendre pourquoi ce segment de schéma est non déterministe, supposons que vous avez le fragment XML non valide suivant :
  
```XML
<container> 
    <aNode/> 
    <aNode/> 
    <anotherNode/> 
</container> 

```

Si vous examinez ce fragment, vous pouvez voir pourquoi il est non valide : il y a deux éléments  `<aNode>` avant l'élément  `<anotherNode>`, alors qu'un seul est autorisé. 
  
Supposons maintenant que vous avez l'instance XML suivante à valider :
  
```XML
<container> 
    <aNode/> 
    <aNode/> 
</container> 

```

Le problème est de déterminer si cette instance est valide. Avez-vous deux éléments  `<aNode>` alors qu'un seul est autorisé, ou avez-vous un élément  `<aNode>` là où il est autorisé et un autre là où il est autorisé ? Le schéma est non déterministe car il n'y a pas de moyen de connaître la réponse. 
  
De la même manière, les éléments facultatifs déclarés dans un élément **xsd:choice** sont généralement problématiques. Dans l'exemple simplifié suivant, il n'y a pas moyen de déterminer si le choix s'est produit une fois avec l'élément facultatif ou s'il ne s'est jamais produit du tout. 
  
```XML
<xsd:choice> 
    <xsd:element name="node" minOccurs="0"/> 
</xsd:choice> 

```

La pratique discutable finale est d'utiliser un élément **xsd:any** sans une définition d'espace de noms, comme dans  `<xsd:any namespace="##other"/>`, après un élément **xsd:sequence**. Cette construction est spécialement gênante lorsqu'elle suit un élément facultatif. Si vous reprenez l'exemple précédent et que vous changez simplement le dernier nœud en un élément **xsd:any**, vous pouvez voir que tous les arguments précédents à propos du non-déterminisme s'appliquent encore, comme suit : 
  
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

## <a name="illegal-enumeration-values"></a>Valeurs d'énumération interdites

Les schémas XSD n'effectuent généralement aucune validation de type tant que vous n'avez pas validé un document d'instance réel. Une exception à cela est le cas où vous avez une énumération dans votre schéma. Dans ce cas, le schéma valide l'énumération par rapport aux types enumeration pour vérifier qu'ils constituent des valeurs correctes pour les nœuds. Voici deux exemples :
  
```XML
<xsd:simpleType name="showTimes"> 
    <xsd:restriction base="xsd:time"> 
        <xsd:enumeration value="18:30:00"/> 
        <xsd:enumeration value="20:45:00"/> 
        <xsd:enumeration value="eleven o'clock"/> 
    </xsd:restriction> 
</xsd:simpleType> 

```

Ce schéma est non valide car "eleven o'clock" n'est pas une valeur valide pour un élément de type **xsd:time**.
  
Voici un exemple plus complexe :
  
```XML
<xsd:simpleType name="concession"> 
    <xsd:restriction base="xsd:NMTOKEN"> 
        <xsd:enumeration value="GummyBears"/> 
        <xsd:enumeration value="SnowCaps"/> 
        <xsd:enumeration value="M&Ms"/> 
    </xsd:restriction> 
</xsd:simpleType> 

```

Pour comprendre pourquoi cet exemple est non valide, vous devez comprendre comment le type **xsd:NMTOKEN** est défini. La spécification des types de données W3C définit le type **NMTOKEN** comme suit : « Un jeton de nom (NMTOKEN) est tout ensemble de caractères de nom ». 
  
Si vous examinez, vous trouvez que « & » n’êtes pas un caractère de nom valide, et par conséquent, « M & Ms » ne valide pas comme type **NMTOKEN** . 
  
## <a name="empty-sequence-or-choice-elements"></a>Éléments sequence ou choice vides

MSXML déclenche parfois des erreurs à propos de déclarations de schéma contenant des éléments **xsd:choice** ou **xsd:sequence** vides, comme dans l'exemple suivant. 
  
```XML
<xsd:element name="emptyContainer"> 
    <xsd:complexType> 
        <xsd:choice /> 
    </xsd:complexType> 
</xsd:element> 

```

La suppression de la balise  `<xsd:choice />` vide doit résoudre ce problème. 
  
## <a name="regular-expressions"></a>Expressions régulières

MSXML 5.0 peut avoir des problèmes pour valider des modèles d'expressions régulières lors du chargement. Les expressions régulières peuvent être compliquées, et vous devez être attentif lorsque vous les utilisez. Chaque analyseur syntaxique XSD semble avoir des langages flexibles pour les expressions régulières : ils implémentent le langage d'expressions régulières XSD officiel ainsi que des éléments provenant d'autres langages d'expressions régulières. Si le concepteur de formulaires d'InfoPath a des problèmes pour analyser une expression régulière, les exemples de données générés par InfoPath peuvent être non valides ou ne pas être générées du tout. Ceci est acceptable lors de la conception, car InfoPath utilise les exemples de données seulement pour la mise en forme. Cependant, si vous utilisez une expression régulière qui n'est pas prise en charge par MSXML, InfoPath ne peut pas valider une valeur par rapport à cette expression lorsqu'un utilisateur remplit un formulaire. [XML Schema Part 0 : Primer Second Edition](http://www.w3.org/TR/xmlschema-0/)décrit ce qui est pris en charge dans les expressions régulières XSD. Pour plus d’informations sur les expressions régulières XSD et les expressions régulières de niveau 1 Unicode, voir [Expressions régulières Unicode](http://www.unicode.org/reports/tr18/) . 
  
## <a name="targetnamespace-attribute-issues"></a>Problèmes liés à l'attribut targetNamespace

XSD est intéressant en ceci que, par défaut, l'attribut **targetNamespace** référence seulement les déclarations du plus haut niveau, bien qu'il soit possible de définir  `attributeFormDefault=qualified` et  `elementFormDefault=qualified` pour remplacer ce comportement par défaut. Par exemple, supposons que vous avez le code XSD suivant. 
  
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

Et supposons que votre document d'instance XML ressemble à l'exemple suivant.
  
```XML
<ns:root xmlns:ns="http://ns"> 
    <local/> 
</ns:root> 

```

Les définitions locales ne requièrent pas d'espace de noms cible car la qualification est désactivée par défaut. Cependant, si vous changez votre définition locale en globale, votre référence doit être qualifiée avec le préfixe d'espace de noms. Par exemple, le schéma suivant est non valide.
  
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

Ce schéma est non valide car "global" est dans l'espace de noms "http://ns". L'élément simple ref="global" n'est pas reconnu car l'espace de noms par défaut n'est pas "http://ns". Pour résoudre cela, vous devez ajouter un préfixe pour l'espace de noms cible et utiliser ceci pour toutes les références globales et les utilisations des types. Le schéma corrigé est similaire à celui-ci.
  
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

Si l'attribut **targetNamespace** est spécifié dans votre schéma, vérifiez que toutes les références globales sont qualifiées avec le préfixe d'espace de noms correct. 
  
## <a name="xml-processing-instruction-encoding-unicode-vs-ansii"></a>Codage des instructions de traitement XML (Unicode ou ANSII)

XML prend en charge seulement les jeux de caractères Unicode. Par conséquent, vous pouvez perdre des informations si vous enregistrez des fichiers qui utilisent des caractères ANSII. L'enregistrement des fichiers au format UTF-16 peut néanmoins être excessif pour votre utilisation spécifique. Pour réduire le coût d'implémentation d'un lecteur XML, le créateur de code XML doit indiquer le codage qu'il utilise dans l'instruction de traitement XML du plus haut niveau. Vous reconnaissez sans doute l'instruction de traitement suivante.
  
```XML
xml version="1.0" encoding="UTF-8"
```

Cette balise d'instruction de traitement spécifie que le codage du fichier est UTF-8. Vous devez vérifier que le codage du fichier est le même que celui qui est indiqué dans cette balise. Vous pouvez déterminer le codage en examinant les octets du fichier et en recherchant les indicateurs Unicode d'ordre des octets. Il existe cependant un moyen plus facile. Si vous avez des problèmes pour ouvrir un schéma XSD, spécifiez un codage « UTF-8 », ouvrez-le dans un éditeur de texte tel que le Bloc-notes, puis enregistrez le fichier avec le codage UTF-8 (le Bloc-notes a une liste déroulante **Codage** dans la boîte de dialogue **Enregistrer sous**). Si vous avez encore des problèmes pour ouvrir le fichier, c'est que ce n'est pas un problème de codage. 
  
## <a name="maxoccurs-attribute-inside-the-xsdall-element"></a>Attribut maxOccurs à l'intérieur d'un élément xsd:all

En raison de la façon dont le non-déterminisme est défini dans la recommandation pour les schémas XML, la seule valeur valide pour l'attribut **maxOccurs** d'un élément **xsd:element** à l'intérieur d'un élément **xsd:all** est 1. Par exemple, le code suivant est valide. 
  
```XML
<xsd:all> 
    <xsd:element name="x" minOccurs="0"/> 
    <xsd:element name="docs" minOccurs="0"/> 
</xsd:all> 

```

Par contre, cet exemple n'est pas valide.
  
```XML
<xsd:all>     
    <xsd:element name="x" minOccurs="0" maxOccurs="unbounded"/> 
    <xsd:element name="docs" minOccurs="0" maxOccurs="unbounded"/> 
</xsd:all> 

```

Cet exemple est non valide car le système de validation ne peut pas déterminer si deux occurrences de  `<x/>` correspondent à la déclaration unique, ou à la déclaration et à une autre définition non valide. Dans les mêmes lignes, vous ne pouvez pas avoir deux éléments du même nom dans une balise  `<xsd:all>`. 
  
Cet exemple est également intéressant car il vous permet d'avoir un nombre quelconque de nœuds  `<x/>` et  `<docs/>` à l'intérieur d'un élément conteneur, dans un ordre quelconque. Bien que cette construction ne soit pas valide, il existe une solution de contournement. En utilisant l'élément **xsd:choice**, vous pouvez obtenir le même résultat, comme le montre l'exemple suivant. 
  
```XML
<xsd:choice minOccurs="0" maxOccurs="unbounded"> 
    <xsd:element name="x" /> 
    <xsd:element name="docs" /> 
</xsd:choice> 

```

## <a name="how-to-edit-or-author-an-xsd-for-infopath"></a>Modification ou création d'un schéma XSD pour InfoPath

Les deux exemples des sections suivantes montrent comment modifier ou créer un schéma pour produire des résultats spécifiques dans InfoPath.
  
## <a name="allowing-user-defined-elements-to-be-inserted-in-the-fields-task-pane"></a>Possibilité d'insérer des éléments définis par l'utilisateur dans le volet Office Champs

Pour permettre à des éléments définis par l'utilisateur d'apparaître sous un élément parent dans le volet Office **Champs**, vous devez insérer un élément **xsd:any** sous l'élément parent. Pour permettre à des éléments définis par l'utilisateur d'être insérés à l'intérieur de  `<your_node_name>`, la déclaration XSD doit être similaire à ce qui suit. 
  
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

Si vous voulez aussi autoriser les attributs définis par l'utilisateur, vous devez ajouter  `<xsd:anyAttribute namespace="##any | ##other"/>` à la déclaration element. 
  
## <a name="allowing-rich-text-elements-to-be-bound-in-infopath-design-and-edit-modes"></a>Possibilité de liaison d'éléments de texte enrichi dans les modes Création et Édition

Si vous voulez déclarer un élément qui peut être lié à un contrôle **Rich Text Box**, il doit avoir la forme suivante, qui inclut l'élément **xsd:any**, qui a un attribut namespace défini à "http://www.w3.org/1999/xhtml", comme le montre l'exemple suivant. 
  
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

## <a name="conclusion"></a>Conclusion

En tirant profit de la prise en charge par InfoPath de la conception de solutions de formulaires XML basées sur des fichiers de schéma XML (.xsd) créés en externe, vous pouvez créer un modèle de formulaire qui fonctionne avec un schéma standard ou avec un schéma créé par votre entreprise ou votre organisation. À l'aide des informations contenues dans cet article, vous pouvez créer des fichiers de schéma XSD qui sont compatibles avec InfoPath, et vous pouvez résoudre des problèmes courants que vous êtes susceptible de rencontrer lorsque vous chargez dans l'environnement de conception InfoPath des fichiers XSD créés en externe.
  
## <a name="see-also"></a>Voir aussi

- [W3C XML Schema (éventuellement en anglais)](http://www.w3.org/XML/Schema)
- [W3C XML Schema Primer (éventuellement en anglais)](http://www.w3.org/TR/xmlschema-0/)
- [W3C XML Schema Structures Reference (éventuellement en anglais)](http://www.xml.com/pub/a/2000/11/29/schemas/structuresref.mdl)
- [W3C XML Schema Datatypes Reference (éventuellement en anglais)](http://www.xml.com/pub/a/2000/11/29/schemas/dataref.mdl)
- [XML Schema Tutorial (éventuellement en anglais)](http://www.w3schools.com/schema/default.asp)
- [Centre d'accès aux données et stockage (éventuellement en anglais)](http://msdn.microsoft.com/en-us/xml/default.aspx)

