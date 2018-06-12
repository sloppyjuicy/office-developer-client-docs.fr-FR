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
description: Accède à l’adresse spécifiée, qui peut être un fichier, UNC ou URL chemin d’accès.
ms.openlocfilehash: 4e86fd3682d5d9e26c52839e76d2016d654b3141
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19788786"
---
# <a name="hyperlink-function"></a>HYPERLINK, fonction

Accède à l’adresse spécifiée, qui peut être un fichier, UNC ou URL chemin d’accès.
  
## <a name="syntax"></a>Syntaxe

Lien hypertexte (« ** *adresse* ** » [, » ** *subaddress* ** «, » ** *extrainfo* ** », ** *fenêtre* **, « ** *cadre* ** »]) 
  
### <a name="parameters"></a>Paramètres

|**Name**|**Obligatoire/Facultatif**|**Type de données**|**Description**|
|:-----|:-----|:-----|:-----|
| _adresse_ <br/> |Obligatoire  <br/> |**Chaîne** <br/> |Chemin d’accès complet ou relatif.  <br/> |
| _sous-adresse_ <br/> |Facultatif  <br/> |**Chaîne** <br/> |Spécifie un emplacement dans address à lier. Par exemple, si l’adresse est un fichier Microsoft Visio, subaddress peut être un nom de la page ; Si un fichier Microsoft Excel, subaddress peut être une feuille de calcul ou une plage dans une feuille de calcul ; Si l’URL d’une page HTML, subaddress peut être un point d’ancrage.  <br/> |
| _ExtraInfo_ <br/> |Facultatif  <br/> |**Chaîne** <br/> |Transmet les informations utilisées pour la résolution de l’URL, comme les coordonnées d’une image interactive.  <br/> |
| _fenêtre_ <br/> |Facultatif  <br/> |**Boolean** <br/> |Indique si le lien hypertexte s’ouvre dans une nouvelle fenêtre. La valeur par défaut est FALSE.  <br/> |
| _cadre_ <br/> |Facultatif  <br/> |**Chaîne** <br/> | Spécifie le nom d’un cadre à cibler lorsque Visio est ouvert comme document ActiveX dans un navigateur ActiveX, tel que Microsoft Internet Explorer 3.0 ou ultérieur. Par défaut, cette chaîne est vide.  <br/> |
   
## <a name="remarks"></a>Note

Si le document n’est pas associé à un chemin d’accès de base, Visio navigue selon le chemin d’accès du document. Si le document n’a pas été enregistré, le lien hypertexte n’est pas défini. 
  
Chemins d’accès relatifs sont basés sur le champ **répertoire Web** spécifié dans la boîte de dialogue **Propriétés Visio** . 
  
Vous pouvez utiliser la fonction GOTOPAGE pour naviguer vers différentes pages d’un document. 
  
## <a name="example-1"></a>Exemple 1

 `HYPERLINK("C:\My Documents\Drawing1.vsdx")`
  
## <a name="example-2"></a>Exemple 2

 `HYPERLINK("\\Server\Share\Drawing1.vsdx")`
  
## <a name="example-3"></a>Exemple 3

 `HYPERLINK("http://www.microsoft.com")`
  
## <a name="example-4"></a>Exemple 4

 `HYPERLINK("..\data.xlsx","sheet1!A1")`
  

