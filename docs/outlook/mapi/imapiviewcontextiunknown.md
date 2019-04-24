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
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: db0c375218755c3a28475e2ebce2d097fb789f75
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32351134"
---
# <a name="imapiviewcontext--iunknown"></a>IMAPIViewContext : IUnknown

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Gère un formulaire dans la visionneuse de formulaires d'une application cliente. 
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |MAPIForm. h  <br/> |
|Exposé par:  <br/> |Afficher les objets de contexte  <br/> |
|Implémenté par :  <br/> |Visionneuses de formulaires  <br/> |
|Appelé par :  <br/> |Objets de formulaires  <br/> |
|Identificateur de l'interface:  <br/> |IID_IMAPIViewContext  <br/> |
|Type de pointeur:  <br/> |LPMAPIVIEWCONTEXT  <br/> |
   
## <a name="vtable-order"></a>Ordre vtable

|||
|:-----|:-----|
|[SetAdviseSink](imapiviewcontext-setadvisesink.md) <br/> |Gère l'inscription d'un formulaire pour recevoir des notifications sur les modifications apportées à la visionneuse.  <br/> |
|[ActivateNext](imapiviewcontext-activatenext.md) <br/> |Active le message suivant ou précédent dans la visionneuse de formulaires.  <br/> |
|[GetPrintSetup](imapiviewcontext-getprintsetup.md) <br/> |Récupère les informations d'impression actuelles.  <br/> |
|[GetSaveStream](imapiviewcontext-getsavestream.md) <br/> |Récupère un flux à utiliser pour enregistrer le message actif.  <br/> |
|[GetViewStatus](imapiviewcontext-getviewstatus.md) <br/> |Récupère l'état actuel de la visionneuse.  <br/> |
|[Généré](imapiviewcontext-getlasterror.md) <br/> |Renvoie une structure [MAPIERROR](mapierror.md) qui contient des informations sur l'erreur précédente qui s'est produite dans l'objet de contexte d'affichage.  <br/> |
   
## <a name="see-also"></a>Voir aussi



[Interfaces MAPI](mapi-interfaces.md)

