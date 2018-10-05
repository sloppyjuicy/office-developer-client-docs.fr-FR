---
title: IPersistMessage IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IPersistMessage
api_type:
- COM
ms.assetid: 40ec6dd4-2206-4e59-aafe-53aaf693f973
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 7eb65bbae2fca6648c3a701dfa5c83c5bf297ec5
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25396182"
---
# <a name="ipersistmessage--iunknown"></a>IPersistMessage : IUnknown

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Permet les visionneuses de formulaire gérer le stockage d’un formulaire et à la transition entre les différents états possibles.
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |MAPIForm.h  <br/> |
|Exposés par :  <br/> |Persistance des objets de message  <br/> |
|Implémenté par :  <br/> |Objets de formulaire  <br/> |
|Appelé par :  <br/> |Visionneuses de formulaire  <br/> |
|Identificateur de l’interface :  <br/> |IID_IPersistMessage  <br/> |
|Type de pointeur :  <br/> |LPPERSISTMESSAGE  <br/> |
   
## <a name="vtable-order"></a>Ordre vtable

|||
|:-----|:-----|
|[GetLastError](ipersistmessage-getlasterror.md) <br/> |Retourne une structure [MAPIERROR](mapierror.md) qui contient des informations sur l’erreur précédente dans l’objet de formulaire.  <br/> |
|[GetClassID](ipersistmessage-getclassid.md) <br/> |Renvoie un identificateur qui représente le serveur de formulaire qui peut gérer le formulaire.  <br/> |
|[IsDirty](ipersistmessage-isdirty.md) <br/> |Vérifie le formulaire pour que les modifications qui ont été apportées depuis le dernier enregistrement.  <br/> |
|[InitNew](ipersistmessage-initnew.md) <br/> |Initialise un nouveau message.  <br/> |
|[Load](ipersistmessage-load.md) <br/> |Charge le formulaire de message spécifié.  <br/> |
|[Save](ipersistmessage-save.md) <br/> |Enregistre un formulaire révisé dans le message à partir de laquelle il a été chargé ou créé.  <br/> |
|[Méthode SaveCompleted](ipersistmessage-savecompleted.md) <br/> |Avertit le formulaire qui un enregistrement opération a été effectuée.  <br/> |
|[HandsOffMessage](ipersistmessage-handsoffmessage.md) <br/> |Le formulaire libérer le message en cours.  <br/> |
   
## <a name="remarks"></a>Remarques

Tous les formulaires sont requis pour implémenter l’interface **IPersistMessage** . 
  
 **IPersistMessage** fonctionne de façon similaire à l’interface OLE [IPersistStorage](https://msdn.microsoft.com/library/1c1a20fc-c101-4cbc-a7a6-30613aa387d7%28Office.15%29.aspx) . Pour plus d’informations, voir les méthodes **IPersistStorage** . 
  
## <a name="see-also"></a>Voir aussi



[Interfaces MAPI](mapi-interfaces.md)

