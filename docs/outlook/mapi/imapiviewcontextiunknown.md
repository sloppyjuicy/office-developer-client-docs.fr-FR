---
title: IMAPIViewContext IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIViewContext
api_type:
- COM
ms.assetid: d566ff39-92c1-4a14-85e5-1c406825f805
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: ae2729ec5620b6b408a5c999d4b6ede7143bed2f
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22584563"
---
# <a name="imapiviewcontext--iunknown"></a>IMAPIViewContext : IUnknown

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
Gère un formulaire dans l’Observateur d’une application cliente formulaire. 
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |MAPIForm.h  <br/> |
|Exposés par :  <br/> |Afficher les objets de contexte  <br/> |
|Implémentée par :  <br/> |Visionneuses de formulaire  <br/> |
|Appelée par :  <br/> |Objets de formulaire  <br/> |
|Identificateur de l’interface :  <br/> |IID_IMAPIViewContext  <br/> |
|Type de pointeur :  <br/> |LPMAPIVIEWCONTEXT  <br/> |
   
## <a name="vtable-order"></a>Ordre vtable

|||
|:-----|:-----|
|[SetAdviseSink](imapiviewcontext-setadvisesink.md) <br/> |Gère l’inscription d’un formulaire pour recevoir des notifications sur les modifications dans la visionneuse.  <br/> |
|[ActivateNext](imapiviewcontext-activatenext.md) <br/> |Active le message suivant ou précédent dans la visionneuse de formulaire.  <br/> |
|[GetPrintSetup](imapiviewcontext-getprintsetup.md) <br/> |Récupère les informations d’impression en cours.  <br/> |
|[GetSaveStream](imapiviewcontext-getsavestream.md) <br/> |Récupère un flux de données à utiliser pour l’enregistrement du message en cours.  <br/> |
|[GetViewStatus](imapiviewcontext-getviewstatus.md) <br/> |Récupère l’état actuel de la visionneuse.  <br/> |
|[GetLastError](imapiviewcontext-getlasterror.md) <br/> |Retourne une structure [MAPIERROR](mapierror.md) qui contient des informations sur l’erreur précédente qui se produisent dans l’objet de contexte de vue.  <br/> |
   
## <a name="see-also"></a>Voir aussi



[Interfaces MAPI](mapi-interfaces.md)

