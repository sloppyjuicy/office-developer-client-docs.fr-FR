---
title: HYPERLINK, fonction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251441
localization_priority: Normal
ms.assetid: 943636a6-e135-a626-7924-11e238156548
description: Accède à l'adresse spécifiée, qui peut être un chemin d'accès de fichier, UNC ou URL.
ms.openlocfilehash: 5e4952c3d56eff0cb1e6518928a7b8259f645046
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32329945"
---
# <a name="hyperlink-function"></a>Fonction HYPERLINK

Accède à l'adresse spécifiée, qui peut être un chemin d'accès de fichier, UNC ou URL.
  
## <a name="syntax"></a>Syntaxe

HYPERLINK ("* * *Address* * *" [, "* ** * SubAddress * *", "* ** * ExtraInfo * *", * * *Window* * *, "* * *Frame* * *"]) 
  
### <a name="parameters"></a>Paramètres

|**Nom**|**Requis/Facultatif**|**Type de données**|**Description**|
|:-----|:-----|:-----|:-----|
| _adresse_ <br/> |Obligatoire  <br/> |**String** <br/> |Chemin d’accès complet ou relatif.  <br/> |
| _SubAddress_ <br/> |Facultatif  <br/> |**Chaîne** <br/> |Spécifie un emplacement dans l'adresse à laquelle établir un lien. Par exemple, si l'adresse est un fichier Microsoft Visio, SubAddress peut être un nom de page; s'il s'agit d'un fichier Microsoft Excel, SubAddress peut être une feuille de calcul ou une plage dans une feuille de calcul; Si une URL pour une page HTML, SubAddress peut être une ancre.  <br/> |
| _InfosSupplémentaires_ <br/> |Facultatif  <br/> |**Chaîne** <br/> |Transmet les informations utilisées pour la résolution de l’URL, comme les coordonnées d’une image interactive.  <br/> |
| _Window_ <br/> |Facultatif  <br/> |**Booléen** <br/> |Indique si le lien hypertexte s’ouvre dans une nouvelle fenêtre. La valeur par défaut est FALSE.  <br/> |
| _fréquence_ <br/> |Facultatif  <br/> |**Chaîne** <br/> | Spécifie le nom d’un cadre à cibler lorsque Visio est ouvert comme document ActiveX dans un navigateur ActiveX, tel que Microsoft Internet Explorer 3.0 ou ultérieur. Par défaut, cette chaîne est vide.  <br/> |
   
## <a name="remarks"></a>Remarques

Si le document n’est pas associé à un chemin d’accès de base, Visio navigue selon le chemin d’accès du document. Si le document n’a pas été enregistré, le lien hypertexte n’est pas défini. 
  
Les chemins d’accès relatifs sont basés sur le champ **Répertoire Web** spécifié dans la boîte de dialogue **Propriétés Visio**. 
  
Vous pouvez utiliser la fonction GOTOPAGE pour naviguer vers différentes pages d’un document. 
  
## <a name="example-1"></a>Exemple 1

 `HYPERLINK("C:\My Documents\Drawing1.vsdx")`
  
## <a name="example-2"></a>Exemple 2

 `HYPERLINK("\\Server\Share\Drawing1.vsdx")`
  
## <a name="example-3"></a>Exemple 3

 `HYPERLINK("https://www.microsoft.com")`
  
## <a name="example-4"></a>Exemple 4

 `HYPERLINK("..\data.xlsx","sheet1!A1")`
  

