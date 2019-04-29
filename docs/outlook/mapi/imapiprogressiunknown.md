---
title: Méthode imapiprogress IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIProgress
api_type:
- COM
ms.assetid: 7a872296-0378-456f-b4d6-cb4d96b09d6e
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 3a3d54ac9485cc3915d3606bb84b4f3191d1ca5b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33419645"
---
# <a name="imapiprogress--iunknown"></a>IMAPIProgress : IUnknown

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Implémente un objet Progress qui fournit aux applications clientes un indicateur de progression. Un indicateur de progression est un affichage d'interface utilisateur qui indique le pourcentage d'achèvement d'une opération, par exemple, la copie de dossiers entre des magasins de messages. Les applications MAPI et client implémentent les objets de progression et les fournisseurs de services les utilisent. 
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapidefs. h  <br/> |
|Exposé par:  <br/> |Objets de progression  <br/> |
|Implémenté par :  <br/> |Applications MAPI et clientes  <br/> |
|Appelé par :  <br/> |Fournisseurs de services  <br/> |
|Identificateur de l'interface:  <br/> |IID_IMAPIProgress  <br/> |
|Type de pointeur:  <br/> |LPMAPIPROGRESS  <br/> |
   
## <a name="vtable-order"></a>Ordre vtable

|||
|:-----|:-----|
|[Progress](imapiprogress-progress.md) <br/> |Met à jour l'indicateur de progression avec un affichage de la progression au fur et à mesure de l'exécution de l'opération.  <br/> |
|[GetFlags](imapiprogress-getflags.md) <br/> |Renvoie les paramètres d'indicateur à partir de l'objet de progression pour le niveau d'opération sur lequel les informations de progression sont calculées.  <br/> |
|[GetMax](imapiprogress-getmax.md) <br/> |Renvoie le nombre maximal d'éléments dans l'opération pour afficher les informations d'avancement.  <br/> |
|[GetMin](imapiprogress-getmin.md) <br/> |Renvoie la valeur minimale de la méthode [SetLimits](imapiprogress-setlimits.md) pour laquelle les informations d'avancement sont affichées.  <br/> |
|[SetLimits](imapiprogress-setlimits.md) <br/> |Définit les limites inférieure et supérieure du nombre d'éléments dans l'opération, ainsi que les indicateurs qui contrôlent le mode de calcul des informations d'avancement pour l'opération.  <br/> |
   
## <a name="remarks"></a>Remarques

MAPI inclut un paramètre _lpProgress_ dans de nombreuses méthodes qui effectuent des opérations potentiellement longues.  _lpProgress_ pointe vers une implémentation cliente d'un objet Progress. Les clients qui implémentent l'interface **méthode imapiprogress** définissent ce paramètre de sorte qu'il pointe vers leur implémentation; les clients qui n'implémentent pas **méthode imapiprogress** définissent le paramètre sur null. Pour afficher un indicateur de progression pendant le traitement de l'opération, les fournisseurs de services utilisent l'objet de progression fourni par le client, le cas échéant, ou une implémentation MAPI (indiquée lorsque _lpProgress_ est défini sur null). 
  
## <a name="mfcmapi-reference"></a>Référence MFCMAPI

Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.
  
|**Files**|**Fonction**|**Commentaire**|
|:-----|:-----|:-----|
|MapiProgress. h et MapiProgress. cpp  <br/> |Non applicable  <br/> |Si le paramètre méthode imapiprogress est activé, MFCMAPI passe une implémentation **méthode imapiprogress** à toutes les fonctions que MFCMAPI appelle et qui acceptent une implémentation.  <br/> |
   
## <a name="see-also"></a>Voir aussi



[MFCMAPI comme un exemple de Code](mfcmapi-as-a-code-sample.md)
  
[Interfaces MAPI](mapi-interfaces.md)

