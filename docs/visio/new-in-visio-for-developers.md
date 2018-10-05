---
title: Nouveautés pour les développeurs Visio 2013
manager: soliver
ms.date: 09/18/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 7e3fb858-0ab8-bd2e-217c-c85b10d79785
description: Ce document fournit une vue d’ensemble des améliorations et ajouts pour les développeurs dans Visio 2013. Pour les développeurs, prêts à commencer sur la plate-forme Visio, il fournit suffisamment de détails pour commencer le codage Visio 2013.
ms.openlocfilehash: df4bc1fa493ee3976c99802400ee52691d05d20a
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25397736"
---
# <a name="new-in-visio-for-developers"></a>Nouveautés pour les développeurs Visio 2013

Ce document fournit une vue d’ensemble des améliorations et ajouts pour les développeurs dans Visio 2013. Pour les développeurs, prêts à commencer sur la plate-forme Visio, il fournit suffisamment de détails pour commencer le codage Visio 2013.
  
## <a name="introduction"></a>Introduction
<a name="vis15_WhatsNew_Intro"> </a>

Visio 2013 fournit une plate-forme unique et puissante pour vos solutions de dessins personnalisées. Nouveaux objets, collections, propriétés, méthodes, énumérations et événements, ainsi que de nouvelles cellules et fonctions ShapeSheet, vous fournissent plus d’options pour définir le comportement des éléments de vos solutions.
  
Parmi les nouvelles fonctionnalités intéressantes pour les développeurs dans Visio 2013 sont le nouveau format de fichier ; mises à jour robustes de thèmes ; modifier la fonctionnalité de forme (ce qui vous permet de remplacer les formes avec un autre) ; nouveaux effets de forme ; améliorations apportées aux commentaires ; co-création dans SharePoint Server 2013 ; découpage d’image personnalisable ; géométrie relative ; prise en charge des données de Business Connectivity Services (BCS) ; mises à jour de Visio Services dans Microsoft SharePoint Server 2013 ; et une fonctionnalité en double page. Cette rubrique fournit un résumé rapide de chacune de ces fonctionnalités et mentionne certains des nouveaux objets Visio et des membres qui sont liées avec les fonctionnalités et exposés dans Visual Basic pour Applications (VBA). Pour plus d’informations sur ces fonctionnalités et l’accompagnement des exemples de code, voir le [Centre pour développeurs Visio](https://msdn.microsoft.com/office/aa905478.aspx).
  
> [!NOTE]
> Visio 2013 inclut plusieurs nouvelles ShapeSheet cellules, lignes et fonctions pour prendre en charge les nouvelles fonctionnalités de Visio. Pour plus d’informations sur les nouveautés dans la feuille ShapeSheet pour Visio 2013, consultez l’article [Nouveautés pour les développeurs Visio ShapeSheet](what-s-new-for-visio-shapesheet-developers.md). 
  
## <a name="new-file-format"></a>Nouveau format de fichier
<a name="vis15_WhatsNew_NewFF"> </a>

Visio 2013 introduit un nouveau format de fichier, en fonction de l’Open Packaging Conventions (OPC) standard (ISO 29500, partie 2) et les éléments XML à partir de l’ancien format de fichier Visio XML (.vdx). Il est un format de fichier compressé, basé sur XML similaire pour les formats de fichier utilisés dans d’autres applications.
  
Étant donné que le nouveau format de fichier est pris en charge par Visio 2013 et Visio Services dans Microsoft SharePoint Server 2013, vous pouvez enregistrer un dessin Visio directement à une bibliothèque SharePoint Server, sans avoir à publier le fichier comme un dessin Web Visio (.vdw). Même dans ce cas, Visio Services peut toujours lire et afficher les fichiers de dessin Web Visio.
  
Le nouveau format de fichier comprend les types de fichiers suivants (à extension) :
  
- .vsdx (dessin Visio)
    
- .vsdm (Dessin Visio prenant en charge les macros)
    
- .vssx (Gabarit Visio)
    
- .vssm (Gabarit Visio prenant en charge les macros)
    
- .vstx (Modèle Visio)
    
- .vstm (Modèle Visio prenant en charge les macros)
    
À l’aide de prise en charge existante pour la lecture et écriture du package de format de fichier (par exemple [System.IO.Packaging](https://msdn.microsoft.com/library/System.IO.Packaging.aspx) ) et pour l’analyse XML ( [System.Xml.Linq](https://msdn.microsoft.com/library/System.Xml.Linq.aspx) ), vous pouvez utiliser par programme les nouveaux formats de fichier. 
  
Visio 2013 conserve la capacité à lire les formats de fichiers anciens (.vsd, .vss, .vst, .vdx, .vsx, .vtx, .vdw, .vwi). Visio 2013 n’enregistre pas au format de fichier Visio XML (.vdx) précédent. Vous devrez à refactoriser pour pouvoir lire le nouveau format de fichier et ses schémas solutions ou les outils qui utilisent les fichiers de format (.vdx) du fichier XML Visio précédentes.
  
Visio Services conserve la possibilité d'afficher le format de dessin Web de Visio (.vdw) dans le navigateur. Elle maintenant restitue également la nouvelle Visio de dessin (.vsdx) et formats Visio prenant en charge les dessins (.vsdm).
  
## <a name="themes"></a>Thèmes
<a name="vis15_WhatsNew_Themes"> </a>

Thèmes ont été repensées dans Visio 2013, en utilisant une plus grande variété d’effets et de styles, y compris l’intégration d’effets artistiques de forme. Les utilisateurs peuvent maintenant décider sur un style principal en appliquant un thème, personnaliser le diagramme avec des variantes de thème et mettre en surbrillance les formes individuelles avec des Styles rapides. Les développeurs ShapeSheet peuvent tirer parti de ces fonctionnalités avec les nouvelles fonctions et des cellules dans la feuille ShapeSheet.
  
Vous pouvez également manipuler des thèmes au niveau de l’objet [Page](https://msdn.microsoft.com/library/7a7f37ab-b448-eb70-b4f1-c185dfbd511e%28Office.15%29.aspx), [forme](https://msdn.microsoft.com/library/da7a8872-4ebb-a607-e0ed-eebf68ff5630%28Office.15%29.aspx)et la [sélection](https://msdn.microsoft.com/library/e5734140-6dbe-7de8-9695-1a22fb4ac628%28Office.15%29.aspx) . Nouvelles API pour l’utilisation des thèmes inclure [Page.SetTheme](https://msdn.microsoft.com/library/5a186f58-9a7a-bd8a-826b-85da75a4d59f%28Office.15%29.aspx) méthode, méthode [Page.SetThemeVariant](https://msdn.microsoft.com/library/8393a95f-83ca-0efa-d987-ae498bfe5e9d%28Office.15%29.aspx) , méthode [Shape.SetQuickStyle](https://msdn.microsoft.com/library/aebe80cb-fae9-0be7-e903-882f6eb58b63%28Office.15%29.aspx) et la méthode [Selection.SetQuickStyle](https://msdn.microsoft.com/library/39b810b5-0738-daed-0103-8a2df07559c6%28Office.15%29.aspx) . 
  
Pour obtenir une liste détaillée des nouvelles API dans Visio 2013, consultez la section [modifications du modèle objet Visio](#vis15_WhatsNew_NewOM) dans cet article. Pour plus d’informations sur les nouvelles cellules ShapeSheet dans Visio 2013, consultez l’article [Nouveautés pour les développeurs Visio ShapeSheet](what-s-new-for-visio-shapesheet-developers.md).
  
## <a name="change-shape"></a>Modifier la forme
<a name="vis15_WhatsNew_ChangeShapes"> </a>

Visio 2013 inclut une solution de remplacement forme API qui vous permet de remplacer une ou plusieurs formes d’une autre forme contenue dans un gabarit, tout en conservant certaines valeurs locales de la forme d’origine, telles que la forme de texte de forme, des données de forme ou la mise en forme d’une forme. Les développeurs de formes peuvent mettre à jour les paramètres de la feuille ShapeSheet de leurs formes personnalisés pour spécifier le comportement de modifier la forme de leurs formes. Parmi les nouvelles API sont les méthodes [Shape.ReplaceShapes](https://msdn.microsoft.com/library/b330a63d-4e3f-0c4d-c38c-6ee806670225%28Office.15%29.aspx) et [Selection.ReplaceShapes](https://msdn.microsoft.com/library/dc278901-77ce-e1fe-c44f-f464bbb1c360%28Office.15%29.aspx) et l’événement [ReplaceShape](https://msdn.microsoft.com/library/26c4e7cb-6618-6d2f-a4be-515584f8cd10%28Office.15%29.aspx) . 
  
Pour obtenir une liste détaillée des nouvelles API dans Visio 2013, consultez la section [modifications du modèle objet Visio](#vis15_WhatsNew_NewOM) dans cet article. Pour plus d’informations sur les nouvelles cellules ShapeSheet dans Visio 2013, consultez l’article [Nouveautés pour les développeurs Visio ShapeSheet](what-s-new-for-visio-shapesheet-developers.md).
  
## <a name="shape-effects"></a>Effets de forme
<a name="vis15_WhatsNew_ShapeEffects"> </a>

Nouveaux effets de forme comme biseau, rotation 3D, glow, réflexion et esquisse ont été ajoutées à Visio 2013. La feuille ShapeSheet inclut les nouvelles cellules pour l’utilisation de ces effets.
  
Pour plus d’informations sur les nouvelles cellules ShapeSheet dans Visio 2013, consultez l’article [Nouveautés pour les développeurs Visio ShapeSheet](what-s-new-for-visio-shapesheet-developers.md).
  
## <a name="commenting"></a>Commentaires
<a name="vis15_WhatsNew_Commenting"> </a>

Visio 2013 inclut une nouvelle structure de commentaire. Commentaires peuvent maintenant être associés à une forme spécifique ou une page. Visio 2013 inclut deux nouveaux objets, [commentaires](https://msdn.microsoft.com/library/f028cc03-0ef1-8017-a936-d30d45211864%28Office.15%29.aspx) et [commentaire](https://msdn.microsoft.com/library/7cd0ee53-6b8d-a03b-ecd6-f6f6dda0f2d4%28Office.15%29.aspx). Nouvelles API pour l’accès par programme aux commentaires contiennent les propriétés [Document.Comments](https://msdn.microsoft.com/library/15a322ad-70eb-1487-701d-76e2fde73309%28Office.15%29.aspx), [Page.Comments](https://msdn.microsoft.com/library/9618c86c-96c0-be95-ee20-5d1b99f4d5e8%28Office.15%29.aspx), [Shape.Comments](https://msdn.microsoft.com/library/498eca91-beb9-b764-0262-a935e5205710%28Office.15%29.aspx)et [Page.ShapeComments](https://msdn.microsoft.com/library/b7d86594-ba1f-627b-222f-905da1b1201e%28Office.15%29.aspx) . 
  
Visio Services inclut APIs JavaScript permettant de lire les commentaires d’une page ou une forme dans un diagramme.
  
Pour obtenir une liste détaillée des nouvelles API dans Visio 2013, consultez la section [modifications du modèle objet Visio](#vis15_WhatsNew_NewOM) dans cet article. 
  
> [!NOTE]
> Commentaires ne sont plus accessibles par le biais de la feuille ShapeSheet. 
  
## <a name="coauthoring"></a>Co-création
<a name="vis15_WhatsNew_Coauthoring"> </a>

Visio 2013 offre la possibilité aux diagrammes co-auteur stockés sur SharePoint ou Microsoft OneDrive. Les développeurs ont accès à l’événement [Document.AfterDocumentMerge](https://msdn.microsoft.com/library/50658da5-592a-4d16-908f-c6abe3050f09%28Office.15%29.aspx) qui fournit des informations sur les modifications de schéma en raison de la co-création. Les développeurs de solution ont également la possibilité de désactiver la co-création en fonction de leurs besoins personnalisés à l’aide de la cellule [NoCoauth](nocoauth-cell-document-properties-section.md) sur la feuille ShapeSheet du Document. 
  
Pour obtenir une liste détaillée des nouvelles API dans Visio 2013, consultez la section [modifications du modèle objet Visio](#vis15_WhatsNew_NewOM) dans cet article. 
  
## <a name="customizable-image-clipping"></a>Découpage d’image personnalisable
<a name="vis15_WhatsNew_ClipImages"> </a>

Visio 2013 prend en charge la définition d’un chemin d’accès du découpage d’Image personnalisé pour rogner les images à une forme. Cela permet d’étendre les capacités de Visio 2010, prise en charge des images de capture d’une manière rectangulaire. Cette fonctionnalité est disponible dans la feuille ShapeSheet, à l’aide de la cellule [ClippingPath](clippingpath-cell-foreign-image-info-section.md) dans la section **Foreign Image Info** . 
  
Pour plus d’informations sur les nouvelles cellules ShapeSheet dans Visio 2013, consultez l’article [Nouveautés pour les développeurs Visio ShapeSheet](what-s-new-for-visio-shapesheet-developers.md).
  
## <a name="relative-geometries"></a>Géométries relatives
<a name="vis15_WhatsNew_RelativeGeometry"> </a>

Dans les versions précédentes de Visio, la géométrie des formes a été définie par les formules qui dépendent de la hauteur ou la largeur de la forme. Par exemple, dans Visio 2010 les sommets d’un grand nombre de formes Visio intégré ont été définis en multipliant la hauteur ou la largeur de la forme par une constante. Ces formes avaient sections **Geometry** incluant des lignes [MoveTo](moveto-row-geometry-section.md) ou [LineTo](lineto-row-geometry-section.md) (par exemple) contenant des formules comme `Width*1` et `Height*0`.
  
Visio 2013 prend désormais en charge la géométrie relative dans la feuille ShapeSheet. Forme développeurs peuvent maintenant utiliser géométries pour spécifier des géométries en tant que valeurs simples ou les formules, multipliez automatiquement à la hauteur ou la largeur. Sommets de la forme peuvent maintenant être exprimés avec les constantes, par exemple, évite d’avoir à express sommets en multiples de la largeur de la forme ou la hauteur. Il est ainsi plus facile pour les développeurs de créer des formes, avec les meilleures performances et des fichiers de taille réduite. Nouvelles lignes incluent les lignes [RelMoveTo](relmoveto-row-geometry-section.md) et [RelLineTo](rellineto-row-geometry-section.md) où les valeurs des cellules **X** et **Y** sont automatiquement multipliés par la largeur ou la hauteur de la forme (respectivement). 
  
Pour plus d’informations sur les nouvelles lignes de feuille ShapeSheet dans Visio 2013, consultez l’article [Nouveautés pour les développeurs Visio ShapeSheet](what-s-new-for-visio-shapesheet-developers.md).
  
## <a name="support-for-business-connectivity-services-bcs-data"></a>Prise en charge des données de Business Connectivity Services (BCS)
<a name="vis15_WhatsNew_BCS"> </a>

Diagrammes Visio 2013 peuvent maintenant être connectés à des listes externes sur des serveurs SharePoint Server 2013. Une liste externe est une source de contenu externe à SharePoint (par exemple, une table SQL Server) qui a été connecté à une liste SharePoint à l’aide de Microsoft Business Connectivity Services (BCS). Visio Services prend en charge la possibilité d’actualiser les diagrammes Visio en tant que les mises à jour des données.
  
Pour plus d’informations sur les nouveautés de Visio Services, voir l’article [Visio Services dans SharePoint 2013](https://msdn.microsoft.com/library/jj164027%28office.15%29.aspx). Pour plus d’informations sur Business Connectivity Services (BCS), voir [Business Connectivity Services dans SharePoint 2013](https://msdn.microsoft.com/library/jj163782%28office.15%29.aspx).
  
## <a name="improvements-in-visio-services"></a>Améliorations apportées à Visio Services
<a name="vis15_WhatsNew_VisioServices"> </a>

Visio Services dans Microsoft SharePoint Server 2013 inclut de nombreuses améliorations. Comme mentionné précédemment, Visio Services prend en charge le nouveau format de fichier Visio (.vsdx et .vsdm). Visio Services a développé l’actualisation des données et le recalcul, y compris la possibilité de recalculer sur un ensemble de tâches. 
  
Pour plus d’informations sur les nouveautés de Visio Services, voir l’article [Visio Services dans SharePoint 2013](https://msdn.microsoft.com/library/jj164027%28office.15%29.aspx).
  
## <a name="duplicate-page"></a>Page en double
<a name="vis15_WhatsNew_DuplicatePage"> </a>

Vous pouvez maintenant copier une page et toutes ses formes au sein du même document dans Visio 2013. En conséquence, l’objet **Page** possède une nouvelle méthode, [en double](https://msdn.microsoft.com/library/394be23b-997d-0da1-b3bd-8278564fb4e0%28Office.15%29.aspx), qui duplique la page et renvoie un nouvel objet **Page** . 
  
## <a name="visio-object-model-changes"></a>Modifications apportées au modèle objet Visio
<a name="vis15_WhatsNew_NewOM"> </a>

Nouveaux objets, propriétés, méthodes et événements ont été ajoutés au modèle d’objet Visio pour fournir la prise en charge de la programmabilité de nouvelles fonctionnalités de Visio 2013. En outre, améliorations du modèle d’objet résoudre les requêtes fréquentes pour les développeurs pour les modifications apportées à la plate-forme Visio.
  
### <a name="new-members"></a>Nouveaux membres

Les membres suivants ont été ajoutés aux objets existants dans le modèle d’objet Visio.
  
 **Le tableau 1. Améliorations du modèle objet Visio**
  
|**Objet ou collection**|**Nouveaux membres**|
|:-----|:-----|
|[Objet application (Visio)](https://msdn.microsoft.com/library/5b3c8939-793f-116f-11b8-1d4170d95a63%28Office.15%29.aspx) <br/> |[Événement Application.AfterReplaceShapes (Visio)](https://msdn.microsoft.com/library/b02de031-086a-41cc-d832-5434b8096444%28Office.15%29.aspx) <br/> |
||[Événement Application.BeforeReplaceShapes (Visio)](https://msdn.microsoft.com/library/fbf44569-0539-9292-ce20-1f9e34238b33%28Office.15%29.aspx) <br/> |
||[Événement Application.QueryCancelReplaceShapes (Visio)](https://msdn.microsoft.com/library/50c0f2a6-f534-f3af-7e83-c865abda8bf9%28Office.15%29.aspx) <br/> |
||[Événement Application.ReplaceShapesCanceled (Visio)](https://msdn.microsoft.com/library/e8eecd64-e4bd-d2c4-b942-c5ff607a4121%28Office.15%29.aspx) <br/> |
|[Objet ApplicationSettings (Visio)](https://msdn.microsoft.com/library/f2e24211-ecc6-e0f5-4c00-fc50f98a3505%28Office.15%29.aspx) <br/> |[Propriété ApplicationSettings.EnterCommitsText (Visio)](https://msdn.microsoft.com/library/ba9ce9fa-d224-cdc3-668d-46c1849911c7%28Office.15%29.aspx) <br/> |
||[Propriété ApplicationSettings.SVGExportFormat (Visio)](https://msdn.microsoft.com/library/9e7ca1cb-5ace-b75b-0e59-61566b9a0169%28Office.15%29.aspx) <br/> |
|[Objet de document (Visio)](https://msdn.microsoft.com/library/21640062-13a2-a2b2-7c61-7e707671207c%28Office.15%29.aspx) <br/> |[Événement Document.AfterDocumentMerge (Visio)](https://msdn.microsoft.com/library/50658da5-592a-4d16-908f-c6abe3050f09%28Office.15%29.aspx) <br/> |
||[Propriété Document.Comments (Visio)](https://msdn.microsoft.com/library/15a322ad-70eb-1487-701d-76e2fde73309%28Office.15%29.aspx) <br/> |
||[Propriété Document.CompatibilityMode (Visio)](https://msdn.microsoft.com/library/98fc00d3-5d2b-218e-9828-b5581ee7313d%28Office.15%29.aspx) <br/> |
|[Objet de documents (Visio)](https://msdn.microsoft.com/library/e9291149-964e-c6fb-4c62-bf2f35a6a0a7%28Office.15%29.aspx) <br/> |[Événement Documents.AfterDocumentMerge (Visio)](https://msdn.microsoft.com/library/cac0544d-77b9-b722-cfdb-e42475ce2558%28Office.15%29.aspx) <br/> |
||[Événement Documents.AfterReplaceShapes (Visio)](https://msdn.microsoft.com/library/e01c069e-440b-7b8b-8d7d-cdb664f6e2d6%28Office.15%29.aspx) <br/> |
||[Événement Documents.BeforeReplaceShapes (Visio)](https://msdn.microsoft.com/library/55a66c47-a2ca-5c8a-2693-aaa1b079c704%28Office.15%29.aspx) <br/> |
||[Événement Documents.QueryCancelReplaceShapes (Visio)](https://msdn.microsoft.com/library/d613730e-04c8-d17f-0ad1-19e976aa107d%28Office.15%29.aspx) <br/> |
||[Événement Documents.ReplaceShapesCanceled (Visio)](https://msdn.microsoft.com/library/94a20fe7-da09-4e3c-d048-05ba0b8f1070%28Office.15%29.aspx) <br/> |
|[Objet InvisibleApp (Visio)](https://msdn.microsoft.com/library/70a30571-2017-af8b-eaa1-bf93c758a46a%28Office.15%29.aspx) <br/> |[Événement InvisibleApp.AfterReplaceShapes (Visio)](https://msdn.microsoft.com/library/5d7b8ec2-ef65-1a49-fb50-3fae95d56761%28Office.15%29.aspx) <br/> |
||[Événement InvisibleApp.BeforeReplaceShapes (Visio)](https://msdn.microsoft.com/library/bd0e37ca-887a-4d53-3b0c-3339492df3dd%28Office.15%29.aspx) <br/> |
||[Événement InvisibleApp.QueryCancelReplaceShapes (Visio)](https://msdn.microsoft.com/library/5e5d9b76-dfd4-1d02-d205-9e64350449d5%28Office.15%29.aspx) <br/> |
||[Événement InvisibleApp.ReplaceShapesCanceled (Visio)](https://msdn.microsoft.com/library/17e43497-c7a8-8546-595c-4630afb301a3%28Office.15%29.aspx) <br/> |
|[Objet page (Visio)](https://msdn.microsoft.com/library/7a7f37ab-b448-eb70-b4f1-c185dfbd511e%28Office.15%29.aspx) <br/> |[Événement Page.AfterReplaceShapes (Visio)](https://msdn.microsoft.com/library/e4005987-acb1-78d7-91fb-c3c2d5b036e3%28Office.15%29.aspx) <br/> |
||[Événement Page.BeforeReplaceShapes (Visio)](https://msdn.microsoft.com/library/57ea9836-74dd-77c2-6541-f8f61b89c0b6%28Office.15%29.aspx) <br/> |
||[Propriété Page.Comments (Visio)](https://msdn.microsoft.com/library/9618c86c-96c0-be95-ee20-5d1b99f4d5e8%28Office.15%29.aspx) <br/> |
||[Méthode Page.Duplicate (Visio)](https://msdn.microsoft.com/library/394be23b-997d-0da1-b3bd-8278564fb4e0%28Office.15%29.aspx) <br/> |
||[Méthode Page.GetTheme (Visio)](https://msdn.microsoft.com/library/31c84e69-0bc8-2d1a-84d8-7397110d74ae%28Office.15%29.aspx) <br/> |
||[Méthode Page.GetThemeVariant (Visio)](https://msdn.microsoft.com/library/40c2be31-fdb0-68ee-a129-2788b1b17c82%28Office.15%29.aspx) <br/> |
||[Événement Page.QueryCancelReplaceShapes (Visio)](https://msdn.microsoft.com/library/17ead23f-825a-c608-3315-e2eed6784cd5%28Office.15%29.aspx) <br/> |
||[Événement Page.ReplaceShapesCanceled (Visio)](https://msdn.microsoft.com/library/867b1fc1-96bd-cbeb-fd61-b02a96e039ca%28Office.15%29.aspx) <br/> |
||[Méthode Page.SetTheme (Visio)](https://msdn.microsoft.com/library/5a186f58-9a7a-bd8a-826b-85da75a4d59f%28Office.15%29.aspx) <br/> |
||[Méthode Page.SetThemeVariant (Visio)](https://msdn.microsoft.com/library/8393a95f-83ca-0efa-d987-ae498bfe5e9d%28Office.15%29.aspx) <br/> |
||[Propriété Page.ShapeComments (Visio)](https://msdn.microsoft.com/library/b7d86594-ba1f-627b-222f-905da1b1201e%28Office.15%29.aspx) <br/> |
|[Objet pages (Visio)](https://msdn.microsoft.com/library/45eec568-b5cc-5e80-ff5c-4dfa567efb5d%28Office.15%29.aspx) <br/> |[Événement Pages.AfterReplaceShapes (Visio)](https://msdn.microsoft.com/library/05c33bdd-e697-d36e-46a8-45705e9ad2c2%28Office.15%29.aspx) <br/> |
||[Événement Pages.BeforeReplaceShapes (Visio)](https://msdn.microsoft.com/library/3f6dbc31-0583-dd67-0432-335d6df7a50c%28Office.15%29.aspx) <br/> |
||[Événement Pages.QueryCancelReplaceShapes (Visio)](https://msdn.microsoft.com/library/d11ff976-0016-da6b-92fb-379baa7e8f94%28Office.15%29.aspx) <br/> |
||[Événement Pages.ReplaceShapesCanceled (Visio)](https://msdn.microsoft.com/library/f0ce8c66-7a15-5f91-8c89-e177bc6671d2%28Office.15%29.aspx) <br/> |
|[Objet Selection (Visio)](https://msdn.microsoft.com/library/e5734140-6dbe-7de8-9695-1a22fb4ac628%28Office.15%29.aspx) <br/> |[Méthode Selection.ReplaceShape (Visio)](https://msdn.microsoft.com/library/dc278901-77ce-e1fe-c44f-f464bbb1c360%28Office.15%29.aspx) <br/> |
||[Méthode Selection.SetQuickStyle (Visio)](https://msdn.microsoft.com/library/39b810b5-0738-daed-0103-8a2df07559c6%28Office.15%29.aspx) <br/> |
|[Objet Shape (Visio)](https://msdn.microsoft.com/library/da7a8872-4ebb-a607-e0ed-eebf68ff5630%28Office.15%29.aspx) <br/> |[Méthode Shape.ChangePicture (Visio)](https://msdn.microsoft.com/library/9193d802-cebd-2bfd-5f8e-400fac36c1a5%28Office.15%29.aspx) <br/> |
||[Propriété Shape.Comments (Visio)](https://msdn.microsoft.com/library/498eca91-beb9-b764-0262-a935e5205710%28Office.15%29.aspx) <br/> |
||[Méthode Shape.ReplaceShape (Visio)](https://msdn.microsoft.com/library/b330a63d-4e3f-0c4d-c38c-6ee806670225%28Office.15%29.aspx) <br/> |
||[Méthode Shape.SetQuickStyle (Visio)](https://msdn.microsoft.com/library/aebe80cb-fae9-0be7-e903-882f6eb58b63%28Office.15%29.aspx) <br/> |
   
### <a name="new-objects-and-enumerations"></a>Nouveaux objets et énumérations

Les objets suivants ont été ajoutés au modèle d’objet Visio.
  
 **Le tableau 2. Ajouts de modèle d’objet Visio**
  
|**Objet**|**Propriétés**|**Méthodes**|
|:-----|:-----|:-----|
|[Objet CoauthMergeEvent (Visio)](https://msdn.microsoft.com/library/eb9425cb-0108-4909-e334-9cd51e5b9303%28Office.15%29.aspx) <br/> |[Propriété CoauthMergeEvent.BaseDocument (Visio)](https://msdn.microsoft.com/library/7ec09a85-6f51-685b-0c87-4b9eb3266773%28Office.15%29.aspx) <br/> [Propriété CoauthMergeEvent.DownloadDocument (Visio)](https://msdn.microsoft.com/library/19239540-cd5a-13ea-3b26-282ac3676abd%28Office.15%29.aspx) <br/> [Propriété CoauthMergeEvent.ObjectType (Visio)](https://msdn.microsoft.com/library/01baa0c2-75b7-2713-9732-1e7a8a7b33aa%28Office.15%29.aspx) <br/> [Propriété CoauthMergeEvent.Stat (Visio)](https://msdn.microsoft.com/library/d8a96b8e-36b5-c61f-8cea-76266f7eed39%28Office.15%29.aspx) <br/> [Propriété CoauthMergeEvent.WorkingDocument (Visio)](https://msdn.microsoft.com/library/0f3c4358-0d63-df7f-12fe-7f378bacca86%28Office.15%29.aspx) <br/> |Aucune  <br/> |
|[Objet Comment (Visio)](https://msdn.microsoft.com/library/f028cc03-0ef1-8017-a936-d30d45211864%28Office.15%29.aspx) <br/> |[Propriété Comment.AssociatedObject (Visio)](https://msdn.microsoft.com/library/e28eed2e-260e-59c9-9b24-631817fe1ae1%28Office.15%29.aspx) <br/> [Propriété Comment.AuthorInitials (Visio)](https://msdn.microsoft.com/library/abc07100-8c5c-9982-674d-40b58c096816%28Office.15%29.aspx) <br/> [Propriété Comment.AuthorName (Visio)](https://msdn.microsoft.com/library/e1da4db8-7a16-16bf-2a5f-be1ac5372d34%28Office.15%29.aspx) <br/> [Propriété Comment.AuthorSipAddress (Visio)](https://msdn.microsoft.com/library/f8d185a9-91b6-471a-3c0e-ffa8a06b36b3%28Office.15%29.aspx) <br/> [Propriété Comment.AuthorSMTPAddress (Visio)](https://msdn.microsoft.com/library/22e04ccc-c524-ca08-d5e2-db68fdb3afb6%28Office.15%29.aspx) <br/> [Propriété Comment.Collapsed (Visio)](https://msdn.microsoft.com/library/9552e379-e351-78d7-e0ed-4f524c3273a1%28Office.15%29.aspx) <br/> [Propriété Comment.CreateDate (Visio)](https://msdn.microsoft.com/library/b643e13e-da12-a992-3a59-99b37f003fb9%28Office.15%29.aspx) <br/> [Propriété Comment.Document (Visio)](https://msdn.microsoft.com/library/d57b1377-b895-1fe1-2f98-ef000fdd9c39%28Office.15%29.aspx) <br/> [Propriété Comment.EditDate (Visio)](https://msdn.microsoft.com/library/4ad13f54-215e-3680-5de6-13715e309fbf%28Office.15%29.aspx) <br/> [Propriété Comment.ObjectType (Visio)](https://msdn.microsoft.com/library/bf0d786d-e1b6-65f1-3112-5dfd4ff324e9%28Office.15%29.aspx) <br/> [Propriété Comment.Stat (Visio)](https://msdn.microsoft.com/library/f457598c-af42-cb83-ecd2-4fd42898ea16%28Office.15%29.aspx) <br/> [Propriété Comment.Text (Visio)](https://msdn.microsoft.com/library/3ec63034-de5f-d9f2-16a5-e06a56883867%28Office.15%29.aspx) <br/> |[Méthode Comment.Delete (Visio)](https://msdn.microsoft.com/library/7762f264-f680-5758-7c35-dfe9067b61ca%28Office.15%29.aspx) <br/> |
|[Objet Comments (Visio)](https://msdn.microsoft.com/library/7cd0ee53-6b8d-a03b-ecd6-f6f6dda0f2d4%28Office.15%29.aspx) <br/> |[Propriété Comments.Count (Visio)](https://msdn.microsoft.com/library/abac02d5-5047-2c9d-5c5c-e2738f99a4a6%28Office.15%29.aspx) <br/> [Propriété Comments.Document (Visio)](https://msdn.microsoft.com/library/507d4698-e282-f8a9-1299-c67945ee5fc4%28Office.15%29.aspx) <br/> [Propriété Comments.Item (Visio)](https://msdn.microsoft.com/library/fed2a079-de87-d5ce-1d74-0bfa5a328441%28Office.15%29.aspx) <br/> [Propriété Comments.ObjectType (Visio)](https://msdn.microsoft.com/library/06544d73-ce00-2c89-1ecb-20541b251d57%28Office.15%29.aspx) <br/> [Propriété Comments.Stat (Visio)](https://msdn.microsoft.com/library/1f5f29b2-236c-91b6-6d25-7bacc37ca96c%28Office.15%29.aspx) <br/> |[Méthode Comments.Add (Visio)](https://msdn.microsoft.com/library/da02de49-8057-7e5c-6b59-0a013e56256d%28Office.15%29.aspx) <br/> [Méthode Comments.DeleteAll (Visio)](https://msdn.microsoft.com/library/50777ed3-553c-90ae-2d30-9dde412fe6b9%28Office.15%29.aspx) <br/> |
|[Objet ReplaceShapesEvent (Visio)](https://msdn.microsoft.com/library/26c4e7cb-6618-6d2f-a4be-515584f8cd10%28Office.15%29.aspx) <br/> |[Propriété ReplaceShapesEvent.ObjectType (Visio)](https://msdn.microsoft.com/library/bcc442f0-aa4e-cd5a-d116-f3fb74459927%28Office.15%29.aspx) <br/> [Propriété ReplaceShapesEvent.ReplaceFlags (Visio)](https://msdn.microsoft.com/library/d0d00891-c794-bd0c-d37e-1ab98c92beab%28Office.15%29.aspx) <br/> [Propriété ReplaceShapesEvent.ReplacementMaster (Visio)](https://msdn.microsoft.com/library/326a1889-8952-b4ac-c5c0-ac4470257c06%28Office.15%29.aspx) <br/> [Propriété ReplaceShapesEvent.SelectionSource (Visio)](https://msdn.microsoft.com/library/f81c0b66-b63b-fc7c-1769-d56a17d5cf78%28Office.15%29.aspx) <br/> [Propriété ReplaceShapesEvent.Stat (Visio)](https://msdn.microsoft.com/library/96f3d382-5dda-7f93-088d-96edc831cd7c%28Office.15%29.aspx) <br/> |Aucune  <br/> |
   
Le tableau suivant répertorie les nouvelles énumérations et des constantes introduites dans Visio 2013.
  
 **Le tableau 3. Ajouts d’énumération Visio**
  
|**Énumération**|**Description**|
|:-----|:-----|
|[Énumération VisQuickStyleColors (Visio)](https://msdn.microsoft.com/library/c19d91f3-a9a4-e31e-ed7a-eef15553fbf4%28Office.15%29.aspx) <br/> |Spécifie les noms désignés des couleurs contenus dans un thème.  <br/> |
|[Énumération VisQuickStyleMatrixIndices (Visio)](https://msdn.microsoft.com/library/0fb0b448-85ba-4fc4-d933-21d574cefa2a%28Office.15%29.aspx) <br/> |Spécifie les noms désignés pour les thèmes et des variantes fournies avec Visio 2013.  <br/> |
|[Énumération VisReplaceFlags (Visio)](https://msdn.microsoft.com/library/cf270178-f939-7eb4-b8e1-3b4153aff221%28Office.15%29.aspx) <br/> |Spécifie les comportements d’une opération de changement de forme.  <br/> |
|[Énumération VisSVGExportFormat (Visio)](https://msdn.microsoft.com/library/d8ca8c3f-41d9-4e9d-8f6d-f5567361b14e%28Office.15%29.aspx) <br/> |Spécifie l’inclusion ou l’exclusion du balisage Visio lors de l’exportation d’un diagramme au format SVG.  <br/> |
   
### <a name="deprecated-objects-and-members"></a>Membres et objets supprimés

Le tableau suivant répertorie les objets obsolètes et les membres introduits dans Visio 2013. Obsolète uniquement objet membres sont répertoriés dans la colonne **membres désapprouvés** . 
  
 **Le tableau 4. Déconseillées de modèle d’objet Visio**
  
|**Objet ou collection**|**Membres obsolètes**|
|:-----|:-----|
|Objet **Window**  <br/> |**PageTabWidth,** propriété  <br/> |
   
## <a name="see-also"></a>Voir aussi
<a name="vis15_WhatsNew_Additional"> </a>

- [Visio pour les développeurs](https://msdn.microsoft.com/office/aa905478.aspx)
    
- [Nouveautés pour les développeurs Visio ShapeSheet](what-s-new-for-visio-shapesheet-developers.md)
    
- [Visio Services dans SharePoint 2013](https://msdn.microsoft.com/library/jj164027%28office.15%29.aspx)
    
- [Nouveautés de Visio (Office.com)](https://office.com/redir/HA102749364.aspx)
    
- [Centre de développement Visio](https://msdn.microsoft.com/office/aa905478.aspx)
    

