---
title: IMAPIProgress IUnknown
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
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 975c01457515a400d1d442fedc432dc000f06665
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19783897"
---
# <a name="imapiprogress--iunknown"></a>IMAPIProgress : IUnknown

  
  
**S’applique à**: Outlook 
  
Implémente un objet de progression qui fournit des applications clientes avec un indicateur de progression. Un indicateur de progression est un affichage de l’interface utilisateur qui indique le pourcentage d’achèvement d’une opération, telles que la copie des dossiers entre les magasins de message. Applications clientes et MAPI implémentent des objets de l’avancement et fournisseurs de services de les utilisent. 
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapidefs.h  <br/> |
|Exposés par :  <br/> |Objets de progression  <br/> |
|Implémentée par :  <br/> |Applications MAPI et client  <br/> |
|Appelée par :  <br/> |Fournisseurs de services  <br/> |
|Identificateur de l’interface :  <br/> |IID_IMAPIProgress  <br/> |
|Type de pointeur :  <br/> |LPMAPIPROGRESS  <br/> |
   
## <a name="vtable-order"></a>Ordre vtable

|||
|:-----|:-----|
|[Progress](imapiprogress-progress.md) <br/> |Met à jour l’indicateur de progression avec un affichage de la progression qu’elle est réalisée vers la fin de l’opération.  <br/> |
|[GetFlags](imapiprogress-getflags.md) <br/> |L’indicateur renvoie les paramètres de l’objet de l’avancement du niveau de l’opération sur lequel les informations d’avancement sont calculées.  <br/> |
|[GetMax](imapiprogress-getmax.md) <br/> |Renvoie le nombre maximal d’éléments dans l’opération de l’avancement des informations s’affichent.  <br/> |
|[GetMin](imapiprogress-getmin.md) <br/> |Renvoie la valeur minimale dans la méthode [SetLimits](imapiprogress-setlimits.md) pour l’avancement des informations s’affichent.  <br/> |
|[SetLimits](imapiprogress-setlimits.md) <br/> |Définit les limites supérieures et inférieures pour le nombre d’éléments dans l’opération et des indicateurs qui déterminent comment les informations d’avancement sont calculées pour l’opération.  <br/> |
   
## <a name="remarks"></a>Remarques

MAPI comprend un paramètre _lpProgress_ dans la plupart des méthodes qui effectuent des opérations potentiellement longues.  _lpProgress_ pointe vers une implémentation de client d’un objet de progression. Les clients qui implémentent l’interface **IMAPIProgress** définissent ce paramètre afin de pointer vers leur implémentation ; les clients qui n’implémentent pas **IMAPIProgress** définissez le paramètre sur NULL. Pour afficher un indicateur de progression lors du traitement de l’opération, fournisseurs de services utilisent l’objet progression fourni par le client, le cas échéant, ou une implémentation de MAPI (indiqué lorsque _lpProgress_ est défini sur NULL). 
  
## <a name="mfcmapi-reference"></a>Référence MFCMAPI

Pour des exemples de code MFCMAPI, voir le tableau suivant.
  
|**Fichiers**|**Fonction**|**Commentaire**|
|:-----|:-----|:-----|
|MapiProgress.h et MapiProgress.cpp  <br/> |Not applicable  <br/> |Si le paramètre IMAPIProgress est activé, MFCMAPI transmet une implémentation **IMAPIProgress** à toutes les fonctions qui appelle MFCMAPI qui acceptent une implémentation.  <br/> |
   
## <a name="see-also"></a>Voir aussi



[MFCMAPI comme un exemple de Code](mfcmapi-as-a-code-sample.md)
  
[Interfaces MAPI](mapi-interfaces.md)

