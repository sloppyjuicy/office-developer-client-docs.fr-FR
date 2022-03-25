---
title: IMAPIViewContext IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPIViewContext
api_type:
- COM
ms.assetid: d566ff39-92c1-4a14-85e5-1c406825f805
description: Gère un formulaire dans la visionneuse de formulaires d’une application cliente pour Outlook 2013 et Outlook 2016.
ms.openlocfilehash: 54c18657cc8c4708500a7983573e33f6766d3378
ms.sourcegitcommit: 138c9e15adc07c6ecd740257872aaee6a1a1a7fd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/25/2022
ms.locfileid: "64405530"
---
# <a name="imapiviewcontext--iunknown"></a>IMAPIViewContext : IUnknown

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Gère un formulaire dans la visionneuse de formulaires d’une application cliente. 
  
|Propriété |Valeur |
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapiform.h  <br/> |
|Exposé par :  <br/> |Afficher les objets de contexte  <br/> |
|Implémenté par :  <br/> |Visionneuses de formulaires  <br/> |
|Appelé par :  <br/> |Objets de formulaires  <br/> |
|Identificateur d’interface :  <br/> |IID_IMAPIViewContext  <br/> |
|Type de pointeur :  <br/> |LPMAPIVIEWCONTEXT  <br/> |
   
## <a name="vtable-order"></a>Ordre des vtables

|Member |Description |
|:-----|:-----|
|[SetAdviseSink](imapiviewcontext-setadvisesink.md) <br/> |Gère l’inscription d’un formulaire pour recevoir des notifications sur les modifications apportées à la visionneuse. |
|[ActivateNext](imapiviewcontext-activatenext.md) <br/> |Active le message suivant ou précédent dans la visionneuse de formulaires. |
|[GetPrintSetup](imapiviewcontext-getprintsetup.md) <br/> |Récupère les informations d’impression actuelles. |
|[GetSaveStream](imapiviewcontext-getsavestream.md) <br/> |Extrait un flux à utiliser pour enregistrer le message actuel. |
|[GetViewStatus](imapiviewcontext-getviewstatus.md) <br/> |Récupère l’état actuel de la visionneuse. |
|[GetLastError](imapiviewcontext-getlasterror.md) <br/> |Renvoie une structure [MAPIERROR](mapierror.md) qui contient des informations sur l’erreur précédente qui s’est produite dans l’objet de contexte d’affichage. |
   
## <a name="see-also"></a>Voir aussi



[Interfaces MAPI](mapi-interfaces.md)

