---
title: IPersistMessage IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IPersistMessage
api_type:
- COM
ms.assetid: 40ec6dd4-2206-4e59-aafe-53aaf693f973
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 1e95a52056f8ad9936e8071176fc2bd55e16acfc
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59587915"
---
# <a name="ipersistmessage--iunknown"></a>IPersistMessage : IUnknown

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Permet aux visionneuses de formulaire de gérer le stockage d’un formulaire et de passer des différents états.
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapiform.h  <br/> |
|Exposé par :  <br/> |Persister les objets de message  <br/> |
|Implémenté par :  <br/> |Objets de formulaires  <br/> |
|Appelé par :  <br/> |Visionneuses de formulaires  <br/> |
|Identificateur d’interface :  <br/> |IID_IPersistMessage  <br/> |
|Type de pointeur :  <br/> |LPPERSISTMESSAGE  <br/> |
   
## <a name="vtable-order"></a>Ordre des vtables

|||
|:-----|:-----|
|[GetLastError](ipersistmessage-getlasterror.md) <br/> |Renvoie une [structure MAPIERROR](mapierror.md) qui contient des informations sur l’erreur précédente dans l’objet de formulaire.  <br/> |
|[GetClassID](ipersistmessage-getclassid.md) <br/> |Renvoie un identificateur qui représente le serveur de formulaires qui peut gérer le formulaire.  <br/> |
|[IsDirty](ipersistmessage-isdirty.md) <br/> |Recherche dans le formulaire les modifications apportées depuis le dernier sauvegarde.  <br/> |
|[InitNew](ipersistmessage-initnew.md) <br/> |Initialise un nouveau message.  <br/> |
|[Load](ipersistmessage-load.md) <br/> |Charge le formulaire pour un message spécifié.  <br/> |
|[Save](ipersistmessage-save.md) <br/> |Enregistre un formulaire révisé dans le message à partir duquel il a été chargé ou créé.  <br/> |
|[SaveCompleted](ipersistmessage-savecompleted.md) <br/> |Avertit le formulaire qu’une opération d’enregistrer a été effectuée.  <br/> |
|[HandsOffMessage](ipersistmessage-handsoffmessage.md) <br/> |Fait en sorte que le formulaire libère son message actuel.  <br/> |
   
## <a name="remarks"></a>Remarques

Tous les formulaires sont requis pour **implémenter l’interface IPersistMessage.** 
  
 **IPersistMessage** fonctionne de la même manière que l’interface OLE [IPersistStorage.](https://msdn.microsoft.com/library/1c1a20fc-c101-4cbc-a7a6-30613aa387d7%28Office.15%29.aspx) Pour plus d’informations, voir les **méthodes IPersistStorage.** 
  
## <a name="see-also"></a>Voir aussi



[Interfaces MAPI](mapi-interfaces.md)

