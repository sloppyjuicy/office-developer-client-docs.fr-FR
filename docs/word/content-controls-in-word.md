---
title: Contrôles de contenu dans Word
manager: soliver
ms.date: 09/10/2015
ms.audience: Developer
keywords:
- contrôles de contenu [word], [Word], les contrôles de contenu quelles sont les nouveautés
localization_priority: Normal
ms.assetid: c0e6dd3b-fae1-453d-a9b4-7f456b5172db
description: Découvrez comment les contrôles de contenu Microsoft Word 2013 activer un plus grand nombre de scénarios de document structuré.
ms.openlocfilehash: 1b0b88da4bc3347ac6748ab57b99d45edd57558d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19790138"
---
# <a name="content-controls-in-word"></a>Contrôles de contenu dans Word

Découvrez comment les contrôles de contenu Microsoft Word 2013 activer un plus grand nombre de scénarios de document structuré.

Cette rubrique fournit des informations sur les modifications apportées aux contrôles de contenu dans Microsoft Word 2013 et les scénarios de document qui permettent de ces modifications.
  
### <a name="structured-documents"></a>Documents structurés
<a name="WordCC_StructuredDocs"> </a>

Les documents structurés sont des documents qui contrôlent où le contenu peut s’afficher dans un document, quel type de contenu peut s’afficher dans le document et si ce contenu peut être modifié.
  
Voici quelques scénarios courants d’un contenu structuré dans Microsoft Word :
  
- Un cabinet d’avocats a besoin de créer des documents qui contiennent des passages juridiques qui ne doivent pas être modifiés par l’utilisateur.
    
- Une entreprise a besoin de créer une page de garde pour les propositions où seuls le titre, l’auteur et la date sont saisis par l’utilisateur.
    
- Une entreprise a besoin de créer des factures dans lesquelles les données du client sont incluses dans des zones prédéfinies.
    
### <a name="using-content-controls-to-structure-a-document"></a>Utilisation des contrôles de contenu pour structurer un document
<a name="WordCC_StructuredDocs"> </a>

Contrôles de contenu sont des entités de Microsoft Word qui agissent comme des conteneurs de contenu spécifique dans un document. Chaque contrôle de contenu peut contenir le contenu tel que des dates, des listes ou des paragraphes de texte mis en forme. Contrôles de contenu vous aident à la création structuré des blocs de contenu et sont conçues pour une utilisation dans les modèles insérer des blocs bien définis dans vos documents, création de documents structurés.
  
Les contrôles de contenu sont idéaux pour la création de documents structurés, car ils vous permettent d’ajuster la position du contenu, de spécifier le type de contenu (par exemple, une date, une image ou du texte), de limiter ou d’activer la modification et d’ajouter une sémantique au contenu.
  
### <a name="content-controls-in-word-2010"></a>Contrôles de contenu dans Word 2010
<a name="WordCC_StructuredDocs"> </a>

Les contrôles de contenu suivants sont disponibles dans Word 2010 :
  
- Texte enrichi
    
- Texte brut
    
- Image
    
- Galerie de blocs de construction
    
- Zone de liste modifiable
    
- Liste déroulante
    
- Date
    
- Case à cocher
    
- Groupe
    
Contrôles de contenu Word 2010 activer les solutions de document structuré potentiels différentes, mais dans Word 2013 contrôles de contenu permettent d’une plage de scénarios.
  
## <a name="content-control-improvements-in-word-2013"></a>Améliorations du contrôle de contenu dans Word 2013
<a name="WordCC_WhatsNew"> </a>

Dans Word 2013, les contrôles de contenu fournissent trois améliorations clés : amélioration de la visualisation, prise en charge pour le mappage XML pour les contrôles de contenu de texte riche et un contrôle de contenu pour le contenu qui se répète.
  
### <a name="improved-visualization"></a>Meilleure visualisation

Word 2013 permet à un contrôle de contenu à afficher dans un des trois états possibles :
  
- Cadre englobant
    
- Balises de début et de fin
    
- Aucun
    
> [!NOTE]
> Si ne pas contraire, cette section traite de la visualisation des contrôles de contenu lorsque le document n’est pas affiché en **Mode Création**. Vous définissez le mode d’affichage pour un contrôle de contenu à l’aide du contrôle de liste déroulante **Afficher** dans la boîte de dialogue **Propriétés du contrôle de contenu** . 
  
**La figure 1. Boîte de dialogue Propriétés du contrôle du contenu**

![Boîte de dialogue Propriétés de contrôle de contenu] (media/DK2_WordCC_Fig01.jpg "Boîte de dialogue Propriétés de contrôle de contenu")
  
Vous pouvez également définir le mode d’affichage pour un contrôle de contenu à l’aide du modèle d’objet Word 2013 (abordé plus loin dans les [membres du modèle objet nouveau Word 2013 contrôle de contenu](#WordCC_NewOM)).
  
### <a name="bounding-box"></a>Cadre englobant
<a name="WordCC_DefaultRendering"> </a>

Le rendu par défaut pour les contrôles de contenu dans Word 2013 consiste à conserver l’apparence des contrôles de contenu lorsqu’ils s’affichent dans Word 2007 et Word 2010 ; Autrement dit, comme une zone de délimitation. Lorsqu’un contrôle de contenu est défini à afficher sous forme **De délimitation de la zone**, l’affichage change en fonction de l’interaction utilisateur suivants :
  
- Lorsque le contrôle de contenu n’est pas activé, aucune visualisation ne se produit
    
- Lorsque vous pointez dessus avec la souris, le contrôle de contenu apparaît sous la forme d’un rectangle ombré
    
**La figure 2. Contrôle de contenu sur pointage avec la souris**

![Contenu du contrôle de la souris sur] (media/DK2_WordCC_Fig02.jpg "Contenu du contrôle de la souris sur")
  
- Lorsque le contrôle de contenu est activé (c’est-à-dire lorsque l’utilisateur clique sur le contrôle de contenu), il s’affiche comme un « cadre englobant » (avec une ligne autour du contenu et le titre, si un titre a été défini)
    
**La figure 3. Contrôle de contenu avec focus**

![Contrôle qui a le focus de contenu] (media/DK2_WordCC_Fig03.jpg "Contrôle qui a le focus de contenu")
  
### <a name="startend-tags"></a>Balises de début et de fin
<a name="WordCC_StartEndTags"> </a>

Lorsque le contrôle de contenu est défini à afficher sous forme de **balise de début/fin**, les balises s’affichent quel que soit l’interaction de l’utilisateur et le titre apparaît jamais ; mais les boutons, telles que le bouton de la **Liste déroulante** , apparaissent sur la souris sur. 
  
**La figure 4. Contrôle de contenu défini pour s’afficher sous forme de balises de début/fin**

![Contrôle de contenu défini pour s’afficher comme début et de fin] (media/DK2_WordCC_Fig04.jpg "Contrôle de contenu défini pour s’afficher comme début et de fin")
  
### <a name="none"></a>Aucun
<a name="WordCC_Invisible"> </a>

Lorsque le contrôle de contenu est défini pour s’afficher en tant **qu’Aucun**, le contrôle de contenu n’est pas affiché.
  
### <a name="content-control-colorization"></a>Colorisation des contrôles de contenu
<a name="WordCC_CCColorization"> </a>

Outre l’activation d’un autre type de l’affichage d’un contrôle de contenu, Word 2013 permet également de définir la couleur d’un contrôle de contenu. Vous définissez la couleur d’un contrôle de contenu à l’aide du bouton **couleur** dans la boîte de dialogue **Propriétés du contrôle de contenu** . 
  
Vous pouvez également définir la couleur d’un contrôle de contenu à l’aide du modèle d’objet Word 2013 (abordé plus loin dans les [membres du modèle objet nouveau Word 2013 contrôle de contenu](#WordCC_NewOM)).
  
**La figure 5. Boîte de dialogue Propriétés du contrôle du contenu**

![Boîte de dialogue Propriétés de contrôle de contenu] (media/DK2_WordCC_Fig05.jpg "Boîte de dialogue Propriétés de contrôle de contenu")
  
### <a name="support-for-xml-mapping-for-rich-text-content-controls"></a>Prise en charge du mappage XML pour les contrôles de contenu de texte enrichi
<a name="WordCC_XMLMapping"> </a>

Word 2013 vous aident à mapper le contenu des contrôles de contenu de texte enrichi et des contrôles de contenu de bloc de construction de document dans le magasin de données XML. Pour ce faire, vous définissez le *mappage XML* pour le contrôle de contenu. Vous pouvez définir cette propriété à l’aide de la méthode **XMLMapping.SetMapping** existante dans le modèle objet. Dans la partie XML personnalisée, le XML personnalisé est stocké comme plat balisage Open XML converti en une chaîne (à l’aide de codage XML standard), afin que celui-ci peut être stocké en tant que texte dans la partie XML personnalisée. Toutefois, le mappage continue de bénéficier de la limitation faire correspondre uniquement pour les feuilles de nœuds ou des attributs. 
  
> [!NOTE]
> Les contrôles de contenu de texte enrichi ne peuvent pas contenir d’autres contrôles de contenu de texte enrichi. S’il en existe un au sein d’un autre (par exemple, suite à une manipulation du format de fichier, d’une opération de copier/coller, etc.), il n’est pas lié tant qu’il est contenu dans un contrôle de texte enrichi mappé. 
  
Pour plus d’informations sur la configuration de mappage XML, consultez la section [membres du modèle objet nouveau Word 2013 contrôle de contenu](#WordCC_NewOM) plus loin dans cette rubrique. 
  
### <a name="supporting-repeating-content"></a>Prise en charge du contenu répétitif
<a name="WordCC_SupportingRepeating"> </a>

En plus des améliorations de la visualisation et la prise en charge pour le mappage XML aux contrôles de contenu de texte enrichi, Word 2013 ajoute également un nouveau contrôle de contenu qui vous permet de répéter le contenu. Le contrôle de contenu de section extensible répète le contenu qu’il contient, y compris les autres contrôles de contenu.
  
Vous insérez le contrôle de contenu répétitif autour de paragraphes entiers ou de lignes de table. Une fois que le contrôle entoure une section, vous pouvez insérer des copies de la section au-dessus ou en dessous de la section contenue.
  
**La figure 6. Menu contextuel de contrôle de contenu section extensible**

![Contexte de contrôle de contenu de section extensible] (media/DK2_WordCC_Fig06.jpg "Contexte de contrôle de contenu de section extensible")
  
Vous pouvez répéter la section insérée en utilisant le contrôle sur la fin du contrôle de contenu (affiché sous la forme d’un bouton avec un signe plus (![signe plus](media/DK2_WordCC_Fig06A.jpg "signe"))) ou en choisissant une commande dans le menu contextuel, comme le montre la Figure 6. Le contenu répété devient une section distincte du contrôle que vous pouvez attribuer un titre à l’aide de la boîte de dialogue **Propriétés du contrôle de contenu** . 
  
**La figure 7. Attribuer un titre de section dans la boîte de dialogue Propriétés du contrôle du contenu**

![Boîte de dialogue Propriétés de contrôle de contenu] (media/DK2_WordCC_Fig07.jpg "Boîte de dialogue Propriétés de contrôle de contenu")
  
Une fois que vous avez accordé la section d’un titre, si vous sélectionnez **Autoriser les utilisateurs à ajouter et supprimer des sections** dans la boîte de dialogue **Propriétés du contrôle de contenu** , les utilisateurs peuvent ajouter ou supprimer la section par un nom. 
  
**La figure 8. Utilisez le menu contextuel de contrôle de contenu section extensible pour supprimer une section**

![Contexte de contrôle de contenu de section extensible] (media/DK2_WordCC_Fig08.jpg "Contexte de contrôle de contenu de section extensible")
  
Lorsqu’un contrôle de contenu répétitif entoure d’autres contrôles de contenu, les contrôles de contenu entourés sont répétés dans chaque nouvel élément ; mais le contenu de tous ces contrôles de contenu est rétabli sur le texte d’espace réservé. Il existe deux exceptions pour lesquelles le contenu des contrôles enfants est conservé : 
  
- Lorsqu’un contrôle enfant est un contrôle répétitif.
    
- Lorsqu’un contrôle enfant présente un mappage XML à un nœud à l’extérieur du contrôle de contenu répétitif.
    
**La figure 9. Contrôle de contenu qui contient les contrôles enfants avant répétition répétitif**

![Répétez les contrôle de contenu avant répétitif] (media/DK2_WordCC_Fig09.jpg "Répétez les contrôle de contenu avant répétitif")
  
**La figure 10. Contrôle de contenu qui contient des contrôles enfants après répétition répétitif**

![Répétez les contrôle de contenu après répétitif] (media/DK2_WordCC_Fig10.jpg "Répétez les contrôle de contenu après répétitif")
  
### <a name="repeating-section-content-controls-around-xml-mapped-controls"></a>Contrôles de contenu répétitif autour de contrôles présentant un mappage XML
<a name="WordCC_RepeatingSectionCCs"> </a>

Pour les mappages XML qui sont contenues dans une section extensible, Word 2013 mappe les comme suit.
  
Si le mappage ne croise pas avec un élément dans le nœud défini dans le cadre d’une chaîne de son parent, la liaison est une « liaison absolue » et affiche le même contenu dans tous les éléments de section extensible.
  
Si le mappage croise avec un élément dans le nœud défini dans le cadre d’une chaîne de son parent, la liaison est une « liaison relative » et est remapper comme suit :
  
- La liaison absolue pour le nœud est déterminée (aplanissement des expressions de requête) ; cela doit se produire sur le mappage initial
    
- L’axe de la liaison qui présente une référence croisée avec le jeu de nœuds est supprimé.
    
- Le reste de l’expression XPath est évalué par rapport à l’expression XPath de l’élément de contenu répétitif
    
Par exemple, les mappages suivants peuvent se produire :
  
- La section répétitive est mappée à \root\next\path
    
- Le contrôle dans l’exemple d’élément est mappé à \root\next\path[2]\baz
    
- Word met en correspondance \root\next\path[2] avec un élément dans le jeu de nœuds
    
La liaison est donc évaluée comme .\baz, où la base est le nœud de l’élément de contenu répétitif.
  
Les suggestions suivantes pour utiliser des contrôles de contenu répétitif peuvent vous aider à éviter de perdre des données et d’être frustré.
  
### <a name="working-with-repeating-section-content-controls-that-are-mapped-to-xml-data"></a>Utilisation des contrôles de contenu répétitif mappés à des données XML
<a name="WordCC_RepeatingSectionCCs"> </a>

Si vous insérez un contrôle de contenu section extensible qui est mappé à des données XML, chaque fois que l’utilisateur rouvre le document, Word recrée les éléments de section extensible, en fonction des informations dans le magasin de données. Même si vous enregistrez le document, les modifications apportées par l’utilisateur dans les éléments de section extensible dans le document qui ne sont pas également mappées dans le magasin de données sont perdues.
  
Pour éviter que cela ne se produise, verrouillez le contrôle de contenu répétitif et n’autorisez l’utilisateur à apporter des modifications qu’aux contrôles de contenu enfants déverrouillés qui sont également mappés aux données XML.
  
### <a name="binding-a-repeating-section-content-control-to-a-table"></a>Liaison d’un contrôle de contenu répétitif à une table
<a name="WordCC_RepeatingSectionCCs"> </a>

Si vous souhaitez lier un contrôle de contenu de section extensible à une table, insérez le tableau, *puis* l’insérer contenu contrôle de section extensible et pas l’inverse. (Dans le cas contraire, vous ne pourrez sélectionnez uniquement la table). 
  
### <a name="nesting-repeating-section-content-controls-within-a-table"></a>Imbrication de contrôles de contenu répétitif dans un tableau
<a name="WordCC_RepeatingSectionCCs"> </a>

L’imbrication étroite de contrôles de contenu répétitif au sein d’une table (par exemple, lorsque la fin du contrôle de contenu répétitif parent et la fin du contrôle de contenu répétitif enfant se trouvent dans la même cellule) entraîne la suppression de la section répétitive extérieure en cas de suppression ou d’ajout d’un élément dans la section intérieure.
  
Vous pouvez éviter cela en ajoutant une marque de paragraphe entre la fin d’un contrôle de contenu de section extensible et le suivant. Pour masquer la marque de paragraphe, désactivez l’option **Afficher/masquer** de l’onglet **accueil** du ruban. 
  
### <a name="open-xml-file-format-schema-additions"></a>Ajouts au schéma au format Open XML
<a name="WordCC"> </a>

Les éléments suivants ont été ajoutés au schéma WordprocessingML au format Open XML.
  
**Le tableau 1. Nouveaux éléments dans le schéma WordprocessingML le Format de fichier Open XML pour les contrôles de contenu**

|**Élément**|**Description**|
|:-----|:-----|
|\<w:Appearance\>  <br/> |\<w:Appearance\> est un élément enfant de \<w:sdtPr\>.  <br/> Voici les valeurs valides pour l’attribut val :  <br/> \<w:Appearance val = boundingBox|balises|masqué.  <br/> La valeur par défaut est boundingBox.  <br/> |
|\<w:Color\>  <br/> |\<w:Color\> est un élément enfant de \<w:sdtPr\>.  <br/> Le modèle de contenu correspond au type complexe CT_Color existant. La valeur par défaut est la couleur utilisée dans Word 2010.  <br/> |
   
## <a name="new-word-2013-content-control-object-model-members"></a>Nouveaux membres du modèle objet Word 2013 contrôle de contenu
<a name="WordCC_NewOM"> </a>

Avec les nouvelles améliorations et ajouts aux contrôles de contenu dans Word 2013, le modèle objet Word a été mis à jour pour permettre la manipulation de l’ensemble des nouvelles fonctionnalités. En outre, les modifications ont également été apportées au Format de fichier XML ouvert sous-jacent pour les documents de traitement de texte.
  
Les sections suivantes fournissent davantage d’informations sur les modifications spécifiques apportées au modèle objet relatives à l’amélioration de chaque contrôle de contenu.
  
### <a name="visualization-enhancements"></a>Améliorations de visualisation
<a name="WordCC_VisEnhancements"> </a>

Plusieurs ajouts de modèle objet sont inclus dans Word 2013 pour les améliorations de visualisation d’un contrôle de contenu. Le tableau suivant répertorie les nouveaux membres de l’objet **ContentControl** pour visualisation. 
  
**Le tableau 2. Nouveaux membres de l’objet ContentControl**

|**Membre**|**Description**|
|:-----|:-----|
|. **Apparence** en tant que **WdContentControlAppearance** <br/> |Obtient ou définit la visualisation du contrôle de contenu.  <br/> |
|. **Couleur** que **WdColor** <br/> |Obtient ou définit la couleur du contrôle de contenu.  <br/> |
   
Le tableau suivant répertorie les constantes de l’énumération **WdContentControlAppearance** nouveau. 
  
**Le tableau 3. Nouvelles constantes d’énumération WdContentControlAppearance**

|**Constante**|**Description**|
|:-----|:-----|
|**wdContentControlBoundingBox** <br/> |Représente un contrôle de contenu affiché sous la forme d’une zone ombrée rectangulaire/englobante (avec un titre facultatif).  <br/> |
|**wdContentControlTags** <br/> |Représente un contrôle de contenu affiché comme des marques de début et de fin.  <br/> |
|**wdContentControlHidden** <br/> |Représente un contrôle de contenu qui n’est pas affiché.  <br/> |
   
### <a name="code-sample"></a>Exemple de code
<a name="WordCC_VisEnhancements"> </a>

L’exemple de code suivant montre comment créer des contrôles de contenu de texte enrichi et définir la visualisation par programme.
  
```vb
Sub testVisualization()
   Dim objcc As ContentControl
   Dim objRange As Range
   
   ' Get the first paragraph as a range object.
   Set objRange = ActiveDocument.Paragraphs(1).Range
   ' Create a rich text content control around the first paragraph.
   Set objcc = ActiveDocument.ContentControls.Add(wdContentControlRichText, objRange)
   objcc.Title = "Default Bounding Box"
   ' Set visualization to the default.
   objcc.Appearance = wdContentControlBoundingBox
   
   ' Create a new paragraph.
   objRange.InsertParagraphAfter
   Set objRange = ActiveDocument.Paragraphs(2).Range
   ' Create a rich text content control around the second paragraph.
   Set objcc = ActiveDocument.ContentControls.Add(wdContentControlRichText, objRange)
   objcc.Title = "Non Bounding"
   ' Set visualization to invisible.
   objcc.Appearance = wdContentControlHidden
   
   ' Create a new paragraph.
   objRange.InsertParagraphAfter
   Set objRange = ActiveDocument.Paragraphs(3).Range
   ' Create a rich text content control around the third paragraph.
   Set objcc = ActiveDocument.ContentControls.Add(wdContentControlRichText, objRange)
   objcc.Title = "Tags Only with Pink color"
   ' Set visualization to Start/End tags with pink color.
   objcc.Appearance = wdContentControlTags
   objcc.Color = wdColorPink
End Sub
```

### <a name="xml-mapping"></a>Mappage XML
<a name="WordCC_XMLMappingOM"> </a>

Aucun ajouts ont été apportées au modèle objet Word 2013 pour prendre en charge le mappage de texte enrichi aux nœuds XML dans le magasin de données du document. Au lieu de cela, utilisez le modèle d’objet existant pour mapper un contrôle de contenu de texte enrichi à un nœud XML dans le magasin de données du document. En outre, aucun modifications ont été apportées au schéma WordprocessingML de Format de fichier Open XML sous-jacent dans le cadre de la prise en charge du contrôle de contenu de texte enrichi nouvellement inclus spécifiquement pour le mappage XML.
  
#### <a name="code-sample"></a>Exemple de code

L’exemple de code suivant montre comment mapper un contrôle de contenu de texte enrichi à un nœud XML par programme.
  
```vb
Sub testRichBinding()
   Dim objRange As Range
   Dim objcc As ContentControl
   Dim objCustomPart As CustomXMLPart
   Dim blnMap As Boolean
   
   ' Add a custom XML part to the data store.
   Set objCustomPart = ActiveDocument.CustomXMLParts.Add
   ' Load XML fragment into the custom XML part.
   objCustomPart.LoadXML ("<x>Rich Text Databinding</x>")
   ' Get the first paragraph as a range object.
   Set objRange = ActiveDocument.Paragraphs(1).Range
   ' Create a rich text content control around the first paragraph.
   Set objcc = ActiveDocument.ContentControls.Add(wdContentControlRichText, objRange)
   ' Bind the XML node to the rich text content control.
   blnMap = objcc.XMLMapping.SetMapping("/x")
   ' Return whether mapping worked.
   MsgBox objcc.XMLMapping.IsMapped
End Sub
```

### <a name="repeating-section-content-controls-represented-in-the-object-model"></a>Contrôles de contenu répétitif représentés dans le modèle objet
<a name="WordCC_RepeatingSection"> </a>

Le contrôle de contenu de section extensible est disponible dans le modèle d’objet à l’aide les ajouts suivants dans l’objet **ContentControl** et les nouveaux objets **RepeatingSectionItem** et **RepeatingSectionItemColl** . Le tableau 4 répertorie les nouveaux membres de l’objet **ContentControl** pour les contrôles de contenu de section extensibles plus importantes. 
  
**Le tableau 4. Membres de l’objet ContentControl**

|**Membre**|**Description**|
|:-----|:-----|
|**AllowInsertDeleteSection** comme **Boolean** <br/> |Obtient ou définit si les utilisateurs peuvent ajouter ou supprimer des sections à partir du contrôle de contenu à l’aide de l’interface utilisateur. Si cette propriété est appelée pour un contrôle de contenu qui n’est pas du type de section extensible, l’appel échoue avec le message d’erreur suivant : « cette propriété peut uniquement être utilisée avec des contrôles de contenu de section extensibles. »  <br/> |
|**RepeatingSectionItemTitle** sous forme de **chaîne** <br/> |Obtient ou définit le nom de la section éléments utilisés dans le menu contextuel extensibles. Si cette propriété est appelée pour un contrôle de contenu qui n’est pas du type de section extensible, l’appel échoue : « cette propriété peut uniquement être utilisée avec des contrôles de contenu de section extensibles. »  <br/> |
|**InsertRepeatingSectionItemBefore** comme **ContentControl** <br/> |Ajoute un élément de section extensible avant l’élément actuel et retourne le nouvel élément de section extensible. Si cette méthode est appelée pour un contrôle de contenu qui n’est pas de type extensible élément section, l’appel échoue : « cette propriété peut uniquement être utilisée avec des contrôles de contenu élément section extensibles. »  <br/> |
|**InsertRepeatingSectionItemAfter** comme **ContentControl** <br/> |Ajoute un élément de section extensible après l’élément actuel et retourne le nouvel élément de section extensible. Si cette méthode est appelée pour un contrôle de contenu qui n’est pas de type extensible élément section, l’appel échoue : « cette propriété peut uniquement être utilisée avec des contrôles de contenu élément section extensibles. »  <br/> |
   
Le tableau 5 répertorie les membres de l’objet **RepeatingSectionItem** plus importantes. 
  
**Tableau 5. Membres de l’objet RepeatingSectionItem**

|**Membre**|**Description**|
|:-----|:-----|
|**Plage** sous forme de **plage** <br/> |Renvoie la plage de l’élément de section extensible spécifié, à l’exception des balises de début et de fin.  <br/> |
|**Supprimer** <br/> |Supprime l’élément répétitif spécifié.  <br/> |
|**InsertItemAfter** en tant que **RepeatingSectionItem** <br/> |Ajoute un élément répétitif après l’élément spécifié et renvoie le nouvel élément.  <br/> |
|**InsertItemBefore** en tant que **RepeatingSectionItem** <br/> |Ajoute un élément répétitif avant l’élément spécifié et renvoie le nouvel élément.  <br/> |
   
Le tableau 6 répertorie les membres de l’objet **RepeatingSectionItemColl** plus importantes. 
  
**Le tableau 6. Membres de l’objet RepeatingSectionItemColl**

|**Membre**|**Description**|
|:-----|:-----|
|**Élément** en tant que **RepeatingSectionItem** <br/> |Renvoie un élément répétitif individuel.  <br/> |
   
Le tableau 7 répertorie le nouveau membre de l’énumération **WdContentControlType** de répétition des contrôles de contenu de section. 
  
**Le tableau 7. Ajout d’énumération WdContentControlType**

|**Constante**|**Description**|
|:-----|:-----|
|**wdContentControlRepeatingSection** <br/> |Représente un contrôle de contenu qui contient un seul élément dans une section répétitive.  <br/> |
   
### <a name="code-sample"></a>Exemple de code
<a name="WordCC_RepeatingSection"> </a>

L’exemple de code suivant montre comment utiliser par programme des contrôles de contenu répétitif.
  
```vb
Sub testRepeatingSectionControl()
   Dim objRange As Range
   Dim objTable As Table
   Dim objCustomPart As CustomXMLPart
   Dim objCC As ContentControl
   Dim objCustomNode As CustomXMLNode
   
   Set objCustomPart = ActiveDocument.CustomXMLParts.Add
   objCustomPart.LoadXML ("<books>" & _
       "<book><title>Everyday Italian</title>" & _
       "<author>Giada De Laurentiis</author></book>" & _
       "<book><title>Harry Potter</title>" & _
       "<author>J K. Rowling</author></book>" & _
       "<book><title>Learning XML</title>" & _
       "<author>Erik T. Ray</author></book></books>")
   
   Set objRange = ActiveDocument.Paragraphs(1).Range
   Set objTable = ActiveDocument.Tables.Add(objRange, 2, 2)
   With objTable.Borders
       .InsideLineStyle = wdLineStyleSingle
       .OutsideLineStyle = wdLineStyleDouble
   End With
   Set objRange = objTable.Cell(1, 1).Range
   Set objCustomNode = objCustomPart.SelectSingleNode("/books[1]/book[1]/title[1]")
   Set objCC = ActiveDocument.ContentControls.Add(wdContentControlText, objRange)
   objCC.XMLMapping.SetMappingByNode objCustomNode
   Set objRange = objTable.Cell(1, 2).Range
   Set objCustomNode = objCustomPart.SelectSingleNode("/books[1]/book[1]/author[1]")
   Set objCC = ActiveDocument.ContentControls.Add(wdContentControlText, objRange)
   objCC.XMLMapping.SetMappingByNode objCustomNode
   Set objRange = objTable.Rows(1).Range
   Set objCC = ActiveDocument.ContentControls.Add(wdContentControlRepeatingSection, objRange)
   objCC.XMLMapping.SetMapping ("/books[1]/book")
End Sub
```

### <a name="open-xml-file-format-changes-for-repeating-section-content-controls"></a>Modifications de format de fichier Open XML pour les contrôles de contenu répétitif
<a name="WordCC_RepeatingSection"> </a>

La représentation sous forme de format de fichier d’un contrôle de contenu de section extensible utilise généralement les mêmes noms d’élément, les valeurs, et ainsi de suite en tant que le balisage XML existant ; Toutefois, le \<sdt\> élément représentant le conteneur de section extensible externe existe dans l’espace de noms Word 2013, pour garantir la compatibilité avec les versions antérieures de Word.
  
Les éléments répétitifs individuels dans le contrôle de contenu répétitif (qui entourent chaque élément) sont enregistrés en tant que contrôles de contenu de texte enrichi à l’aide de la représentation WordprocessingML existante. Le tableau 8 répertorie les nouveaux éléments dans le schéma WordprocessingML pour les contrôles de contenu répétitif.
  
**Le tableau 8. Contrôles de contenu de nouveaux éléments dans le schéma WordprocessingML de section extensible**

|**Élément**|**Description**|
|:-----|:-----|
|\<w15:repeatingSection\>  <br/> |Spécifie un contrôle de contenu répétitif. Cet élément est incompatible avec tous les autres types de contrôles et n’a ni attributs enfants, ni éléments.  <br/> |
|\<w15:repeatingSectionItem\>  <br/> |Spécifie un contrôle de contenu d’élément répétitif. Cet élément est incompatible avec tous les autres types de contrôles et n’a ni attributs enfants, ni éléments enfants.  <br/> |
|\<w15:doNotAllowInsertDeleteSection\>  <br/> |Spécifie que l’utilisateur ne peut pas ajouter ou supprimer des sections à l’aide de l’interface utilisateur dans Word 2013.  <br/> |
|\<w15:sectionTitle\>  <br/> |Spécifie le nom des éléments de section répétitive (et est utilisé dans le menu contextuel lorsque le contrôle est sélectionné).  <br/> |
   

  

