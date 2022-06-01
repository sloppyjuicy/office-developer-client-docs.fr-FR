---
title: IMAPIFormAdviseSink IUnknown
description: IMAPIFormAdviseSinkIUnknown permet aux serveurs de formulaires de recevoir des notifications des visionneuses de formulaires. Cet article décrit sa syntaxe, son ordre de table virtuelle et ses remarques.
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPIFormAdviseSink
api_type:
- COM
ms.assetid: 180022af-4c1c-408c-a3fe-ed075cef79ab
ms.openlocfilehash: 8e6be6f9d969245caa3efebca0a40a9992490112
ms.sourcegitcommit: f872848fbeb5b2353179ad4bf4eab23f61f87666
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/01/2022
ms.locfileid: "65812200"
---
# <a name="imapiformadvisesink--iunknown"></a>IMAPIFormAdviseSink : IUnknown

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Permet aux serveurs de formulaires de recevoir des notifications de la part des visionneuses de formulaires. 
  
|Propriété |Valeur |
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapiform.h  <br/> |
|Exposé par :  <br/> |Formulaire conseiller les objets récepteurs  <br/> |
|Implémenté par :  <br/> |Serveurs de formulaires  <br/> |
|Appelé par :  <br/> |Visionneuses de formulaires  <br/> |
|Identificateur d’interface :  <br/> |IID_IMAPIFormAdviseSink  <br/> |
|Type de pointeur :  <br/> |LPMAPIFORMADVISESINK  <br/> |
   
## <a name="vtable-order"></a>Ordre des tables virtuelles

|Member |Description |
|:-----|:-----|
|[OnChange](imapiformadvisesink-onchange.md) <br/> |Indique qu’une modification s’est produite dans l’état de la visionneuse de formulaires. |
|[OnActivateNext](imapiformadvisesink-onactivatenext.md) <br/> |Indique si le formulaire peut gérer la classe de message du message suivant à afficher. |
   
## <a name="remarks"></a>Remarques

Les serveurs de formulaires utilisent un objet récepteur form advise pour implémenter **IMAPIFormAdviseSink** au lieu de l’inclure avec leur objet de formulaire. Par conséquent, les observateurs de formulaires doivent s’attendre à un appel ayant échoué à la méthode [IUnknown::QueryInterface](https://msdn.microsoft.com/library/ms682521%28v=VS.85%29.aspx) d’un formulaire pour obtenir un pointeur vers cette interface. 
  
Les serveurs de formulaires appellent la méthode [IMAPIViewContext::SetAdviseSink](imapiviewcontext-setadvisesink.md) d’une visionneuse pour s’inscrire aux notifications. Un pointeur vers son implémentation **IMAPIFormAdviseSink** est inclus en tant que paramètre. 
  
## <a name="see-also"></a>Voir aussi



[Interfaces MAPI](mapi-interfaces.md)

