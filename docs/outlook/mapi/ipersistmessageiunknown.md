---
title: IPersistMessage IUnknown
description: IPersistMessage IUnknown permet aux visionneuses de formulaires de gérer le stockage d’un formulaire et de passer d’un état à l’autre.
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
ms.openlocfilehash: 388315a148bc39853b02f1b06edef986f5e540be
ms.sourcegitcommit: e2b79cc4469013a4b3705620a93aa70b88e6c996
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/02/2022
ms.locfileid: "65826903"
---
# <a name="ipersistmessage--iunknown"></a>IPersistMessage : IUnknown

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Permet aux visionneuses de formulaires de gérer le stockage d’un formulaire et de passer d’un état à l’autre.
  
|Propriété|Valeur|
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapiform.h  <br/> |
|Exposé par :  <br/> |Conserver les objets de message  <br/> |
|Implémenté par :  <br/> |Objets de formulaires  <br/> |
|Appelé par :  <br/> |Visionneuses de formulaires  <br/> |
|Identificateur d’interface :  <br/> |IID_IPersistMessage  <br/> |
|Type de pointeur :  <br/> |LPPERSISTMESSAGE  <br/> |
   
## <a name="vtable-order"></a>Ordre des tables virtuelles

|Member|Description|
|:-----|:-----|
|[Getlasterror](ipersistmessage-getlasterror.md) <br/> |Retourne une structure [MAPIERROR](mapierror.md) qui contient des informations sur l’erreur précédente dans l’objet de formulaire. |
|[GetClassID](ipersistmessage-getclassid.md) <br/> |Retourne un identificateur qui représente le serveur de formulaires qui peut gérer le formulaire. |
|[IsDirty](ipersistmessage-isdirty.md) <br/> |Recherche dans le formulaire les modifications qui ont été apportées depuis le dernier enregistrement. |
|[InitNew](ipersistmessage-initnew.md) <br/> |Initialise un nouveau message. |
|[Load](ipersistmessage-load.md) <br/> |Charge le formulaire pour un message spécifié. |
|[Save](ipersistmessage-save.md) <br/> |Enregistre un formulaire révisé dans le message à partir duquel il a été chargé ou créé. |
|[SaveCompleted](ipersistmessage-savecompleted.md) <br/> |Notifie le formulaire qu’une opération d’enregistrement a été effectuée. |
|[HandsOffMessage](ipersistmessage-handsoffmessage.md) <br/> |Fait en sorte que le formulaire libère son message actuel. |
   
## <a name="remarks"></a>Remarques

Tous les formulaires sont nécessaires pour implémenter l’interface **IPersistMessage** . 
  
 **IPersistMessage** fonctionne de la même façon que l’interface OLE [IPersistStorage](https://msdn.microsoft.com/library/1c1a20fc-c101-4cbc-a7a6-30613aa387d7%28Office.15%29.aspx) . Pour plus d’informations, consultez les méthodes **IPersistStorage** . 
  
## <a name="see-also"></a>Voir aussi



[Interfaces MAPI](mapi-interfaces.md)

