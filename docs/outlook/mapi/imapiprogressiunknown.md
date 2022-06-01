---
title: IMAPIProgress IUnknown
description: IMAPIProgressIUnknown implémente un objet de progression qui fournit aux applications clientes un indicateur de progression.
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPIProgress
api_type:
- COM
ms.assetid: 7a872296-0378-456f-b4d6-cb4d96b09d6e
ms.openlocfilehash: 278296bd2715d305cac4de071a527399379a05bb
ms.sourcegitcommit: f872848fbeb5b2353179ad4bf4eab23f61f87666
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/01/2022
ms.locfileid: "65817717"
---
# <a name="imapiprogress--iunknown"></a>IMAPIProgress : IUnknown

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Implémente un objet de progression qui fournit aux applications clientes un indicateur de progression. Un indicateur de progression est un affichage d’interface utilisateur qui indique le pourcentage d’achèvement d’une opération, tel que la copie de dossiers entre les magasins de messages. MapI et les applications clientes implémentent des objets de progression et les fournisseurs de services les utilisent. 
  
|Propriété |Valeur |
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapidefs.h  <br/> |
|Exposé par :  <br/> |Objets de progression  <br/> |
|Implémenté par :  <br/> |MAPI et applications clientes  <br/> |
|Appelé par :  <br/> |Fournisseurs de services  <br/> |
|Identificateur d’interface :  <br/> |IID_IMAPIProgress  <br/> |
|Type de pointeur :  <br/> |LPMAPIPROGRESS  <br/> |
   
## <a name="vtable-order"></a>Ordre des tables virtuelles

|Member |Description |
|:-----|:-----|
|[Progress](imapiprogress-progress.md) <br/> |Met à jour l’indicateur de progression avec un affichage de la progression à mesure qu’il est effectué vers la fin de l’opération. |
|[GetFlags](imapiprogress-getflags.md) <br/> |Retourne les paramètres d’indicateur de l’objet de progression pour le niveau d’opération sur lequel les informations de progression sont calculées. |
|[GetMax](imapiprogress-getmax.md) <br/> |Retourne le nombre maximal d’éléments de l’opération pour lesquels les informations de progression sont affichées. |
|[GetMin](imapiprogress-getmin.md) <br/> |Retourne la valeur minimale dans la méthode [SetLimits](imapiprogress-setlimits.md) pour laquelle les informations de progression sont affichées. |
|[SetLimits](imapiprogress-setlimits.md) <br/> |Définit les limites inférieure et supérieure pour le nombre d’éléments de l’opération, ainsi que les indicateurs qui contrôlent la façon dont les informations de progression sont calculées pour l’opération. |
   
## <a name="remarks"></a>Remarques

MAPI inclut un paramètre  _lpProgress_ dans la plupart des méthodes qui effectuent des opérations potentiellement longues.  _lpProgress_ pointe vers une implémentation cliente d’un objet de progression. Les clients qui implémentent l’interface **IMAPIProgress** définissent ce paramètre pour qu’il pointe vers leur implémentation ; les clients qui n’implémentent pas **IMAPIProgress** définissent le paramètre sur NULL. Pour afficher un indicateur de progression pendant le traitement de l’opération, les fournisseurs de services utilisent l’objet de progression fourni par le client, le cas échéant, ou une implémentation MAPI (indiquée lorsque  _lpProgress_ a la valeur NULL). 
  
## <a name="mfcmapi-reference"></a>Référence MFCMAPI

Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.
  
|**Files**|**Fonction**|**Commentaire**|
|:-----|:-----|:-----|
|MapiProgress.h et MapiProgress.cpp  <br/> |Non applicable  <br/> |Si le paramètre IMAPIProgress est activé, MFCMAPI transmet une implémentation **IMAPIProgress** à toutes les fonctions appelées par MFCMAPI qui acceptent une implémentation. |
   
## <a name="see-also"></a>Voir aussi



[MFCMAPI comme un exemple de Code](mfcmapi-as-a-code-sample.md)
  
[Interfaces MAPI](mapi-interfaces.md)

