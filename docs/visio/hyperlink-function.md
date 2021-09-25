---
title: HYPERLINK, fonction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251441
ms.localizationpriority: medium
ms.assetid: 943636a6-e135-a626-7924-11e238156548
description: Permet d’accéder à l’adresse spécifiée, qui peut être un fichier, un unc ou un chemin d’URL.
ms.openlocfilehash: 9443f30143a3beb19e31519d0dbe0845ddfd5451
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59554704"
---
# <a name="hyperlink-function"></a>Fonction HYPERLINK

Permet d’accéder à l’adresse spécifiée, qui peut être un fichier, un unc ou un chemin d’URL.
  
## <a name="syntax"></a>Syntaxe

HYPERLINK( » ** *address* ** « [, » ** *subaddress* ** « , » ** *extrainfo* ** « , ** *window* **, » ** *frame* ** « ]) 
  
### <a name="parameters"></a>Paramètres

|**Nom**|**Requis/Facultatif**|**Type de données**|**Description**|
|:-----|:-----|:-----|:-----|
| _adresse_ <br/> |Obligatoire  <br/> |**String** <br/> |Chemin d’accès complet ou relatif.  <br/> |
| _sous-adresse_ <br/> |Facultatif  <br/> |**Chaîne** <br/> |Spécifie un emplacement dans address auquel se lier. Par exemple, si address est un fichier Microsoft Visio, subaddress peut être un nom de page. S’il s’agit d’un fichier Microsoft Excel, subaddress peut être une feuille de calcul ou une plage d’une feuille de calcul. Dans le cas d’une URL permettant d’accéder à une page HTML, subaddress peut être un point d’ancrage.  <br/> |
| _extrainfo_ <br/> |Facultatif  <br/> |**Chaîne** <br/> |Transmet les informations utilisées pour la résolution de l’URL, comme les coordonnées d’une image interactive.  <br/> |
| _window_ <br/> |Facultatif  <br/> |**Boolean** <br/> |Indique si le lien hypertexte s’ouvre dans une nouvelle fenêtre. La valeur par défaut est FALSE.  <br/> |
| _frame_ <br/> |Facultatif  <br/> |**Chaîne** <br/> | Spécifie le nom d’un cadre à cibler lorsque Visio est ouvert comme document ActiveX dans un navigateur ActiveX, tel que Microsoft Internet Explorer 3.0 ou ultérieur. Par défaut, cette chaîne est vide.  <br/> |
   
## <a name="remarks"></a>Remarques

Si le document n’est pas associé à un chemin d’accès de base, Visio navigue selon le chemin d’accès du document. Si le document n’a pas été enregistré, le lien hypertexte n’est pas défini. 
  
Les chemins d’accès relatifs sont basés sur le champ **Répertoire Web** spécifié dans la boîte de dialogue **Propriétés Visio**. 
  
Vous pouvez utiliser la fonction GOTOPAGE pour naviguer vers différentes pages d’un document. 
  
## <a name="example-1"></a>Exemple 1

 `HYPERLINK("C:\My Documents\Drawing1.vsdx")`
  
## <a name="example-2"></a>Exemple 2

 `HYPERLINK("\\Server\Share\Drawing1.vsdx")`
  
## <a name="example-3"></a>Exemple 3

 `HYPERLINK("https://www.microsoft.com")`
  
## <a name="example-4"></a>Exemple 4

 `HYPERLINK("..\data.xlsx","sheet1!A1")`
  

