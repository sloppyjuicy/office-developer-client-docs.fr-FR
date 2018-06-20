---
title: Fonction de la langue
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: e372c670-e9a0-4352-b70a-3a054b036124
description: Permet les opérations de comparaison entre les représentations de langue différente. Il convient de conversion des valeurs de balises (BCP 47) langue Internet Engineering Task Force en identifiants de paramètres régionaux (LCID).
ms.openlocfilehash: 6a05a850f5908ac5a4f6a4a72b2ce56b4c98f137
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19788921"
---
# <a name="language-function"></a>Fonction de la langue

Permet les opérations de comparaison entre les représentations de langue différente. Il convient de conversion des valeurs de balises (BCP 47) langue Internet Engineering Task Force en identifiants de paramètres régionaux (LCID).
  
## <a name="version-information"></a>Informations de version

Version ajoutée : Visio 2013 
  
## <a name="syntax"></a>Syntaxe

 **Langue** ( _lcid_or_bcp47_)
  
### <a name="parameters"></a>Paramètres

|**Name**|**Obligatoire/Facultatif**|**Type de données**|**Description**|
|:-----|:-----|:-----|:-----|
| _lcid_or_bcp47_ <br/> |Obligatoire  <br/> |**Chaîne** <br/> |La valeur LCID ou norme BCP 47 pour la langue.  <br/> |
   
## <a name="return-value"></a>Valeur renvoy�e

Entier
  
## <a name="example"></a>Exemple

 `LANGUAGE("en-us")`
  
Renvoie la valeur « 1033 ».
  
 `LANGUAGE("es-es")`
  
Renvoie la valeur « 3082 ».
  

