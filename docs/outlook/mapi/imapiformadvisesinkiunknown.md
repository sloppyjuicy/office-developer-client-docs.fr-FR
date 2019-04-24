---
title: IMAPIFormAdviseSink IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFormAdviseSink
api_type:
- COM
ms.assetid: 180022af-4c1c-408c-a3fe-ed075cef79ab
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 68c2af0cd8d7ccddf6aa6017cfb830b196ac0771
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32286603"
---
# <a name="imapiformadvisesink--iunknown"></a>IMAPIFormAdviseSink : IUnknown

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Permet aux serveurs de formulaires de recevoir des notifications des observateurs de formulaires. 
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |MAPIForm. h  <br/> |
|Exposé par:  <br/> |Objets de récepteur de formulaire advise  <br/> |
|Implémenté par :  <br/> |Serveurs de formulaires  <br/> |
|Appelé par :  <br/> |Visionneuses de formulaires  <br/> |
|Identificateur de l'interface:  <br/> |IID_IMAPIFormAdviseSink  <br/> |
|Type de pointeur:  <br/> |LPMAPIFORMADVISESINK  <br/> |
   
## <a name="vtable-order"></a>Ordre vtable

|||
|:-----|:-----|
|[OnChange](imapiformadvisesink-onchange.md) <br/> |Indique qu'une modification a eu lieu dans l'état de la visionneuse de formulaires.  <br/> |
|[OnActivateNext](imapiformadvisesink-onactivatenext.md) <br/> |Indique si le formulaire peut gérer la classe de message du prochain message à afficher.  <br/> |
   
## <a name="remarks"></a>Remarques

Les serveurs de formulaires utilisent un objet récepteur de formulaire pour implémenter **IMAPIFormAdviseSink** au lieu de l'inclure dans l'objet Form. Par conséquent, les visionneuses de formulaires doivent attendre un appel ayant échoué à la méthode [IUnknown:: QueryInterface](https://msdn.microsoft.com/library/ms682521%28v=VS.85%29.aspx) d'un formulaire pour obtenir un pointeur vers cette interface. 
  
Les serveurs de formulaires appellent la méthode [IMAPIViewContext:: SetAdviseSink](imapiviewcontext-setadvisesink.md) de la visionneuse pour s'inscrire aux notifications. Un pointeur vers son implémentation **IMAPIFormAdviseSink** est inclus en tant que paramètre. 
  
## <a name="see-also"></a>Voir aussi



[Interfaces MAPI](mapi-interfaces.md)

