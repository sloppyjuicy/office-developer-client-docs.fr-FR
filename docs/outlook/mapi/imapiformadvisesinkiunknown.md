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
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 68c2af0cd8d7ccddf6aa6017cfb830b196ac0771
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25392059"
---
# <a name="imapiformadvisesink--iunknown"></a>IMAPIFormAdviseSink : IUnknown

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Permet aux serveurs de formulaire de recevoir des notifications de visionneuses de formulaire. 
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |MAPIForm.h  <br/> |
|Exposés par :  <br/> |Objets de récepteur de notification de formulaire  <br/> |
|Implémenté par :  <br/> |Serveurs de formulaire  <br/> |
|Appelé par :  <br/> |Visionneuses de formulaire  <br/> |
|Identificateur de l’interface :  <br/> |IID_IMAPIFormAdviseSink  <br/> |
|Type de pointeur :  <br/> |LPMAPIFORMADVISESINK  <br/> |
   
## <a name="vtable-order"></a>Ordre vtable

|||
|:-----|:-----|
|[OnChange](imapiformadvisesink-onchange.md) <br/> |Indique qu’une modification s’est produite dans l’état de la visionneuse de formulaire.  <br/> |
|[OnActivateNext](imapiformadvisesink-onactivatenext.md) <br/> |Indique si le formulaire peut gérer la classe de message du message suivant à afficher.  <br/> |
   
## <a name="remarks"></a>Remarques

Écran serveurs utilisent un formulaire de notification objet récepteur d’implémenter **IMAPIFormAdviseSink** au lieu d’y compris avec l’objet de formulaire. Par conséquent, les visionneuses de formulaire être confronté à un appel ayant échoué à la méthode [IUnknown::QueryInterface](https://msdn.microsoft.com/library/ms682521%28v=VS.85%29.aspx) d’un formulaire pour obtenir un pointeur vers cette interface. 
  
Serveurs de formulaire appellent la méthode de [IMAPIViewContext::SetAdviseSink](imapiviewcontext-setadvisesink.md) d’un utilisateur pour s’inscrire pour les notifications. Un pointeur vers leur mise en oeuvre **IMAPIFormAdviseSink** est inclus en tant que paramètre. 
  
## <a name="see-also"></a>Voir aussi



[Interfaces MAPI](mapi-interfaces.md)

