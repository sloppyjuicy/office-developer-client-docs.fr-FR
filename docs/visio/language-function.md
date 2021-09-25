---
title: LANGUAGE Function
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: e372c670-e9a0-4352-b70a-3a054b036124
description: Permet d’établir des opérations de comparaison entre différentes représentations linguistiques. Il est préférable pour convertir des balises de langue BCP 47 (Internet Engineering Task Force) en valeurs d’ID de paramètres régionaux (LCID).
ms.openlocfilehash: 319d1a043b43f80accfe5b195a640acaea5a1c52
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59554515"
---
# <a name="language-function"></a>LANGUAGE Function

Permet d’établir des opérations de comparaison entre différentes représentations linguistiques. Il est préférable pour convertir des balises de langue BCP 47 (Internet Engineering Task Force) en valeurs d’ID de paramètres régionaux (LCID).
  
## <a name="version-information"></a>Informations de version

Version ajoutée : Visio 2013
 
  
## <a name="syntax"></a>Syntaxe

 **LANGUAGE**( _lcid_or_bcp47_)
  
### <a name="parameters"></a>Paramètres

|**Nom**|**Requis/Facultatif**|**Type de données**|**Description**|
|:-----|:-----|:-----|:-----|
| _lcid_or_bcp47_ <br/> |Obligatoire  <br/> |**String** <br/> |Valeur LCID ou BCP 47 pour la langue.  <br/> |
   
## <a name="return-value"></a>Valeur renvoyée

Entier
  
## <a name="example"></a>Exemple

 `LANGUAGE("en-us")`
  
Renvoie la valeur « 1033 ».
  
 `LANGUAGE("es-es")`
  
Renvoie la valeur « 3082 ».
  

