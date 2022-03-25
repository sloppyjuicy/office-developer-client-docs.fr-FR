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
ms.openlocfilehash: e51eb3ef17eef016e82739e09d20a60deec89675
ms.sourcegitcommit: eb9453e5664b01759b602cb5a4cef5b4885128f3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/24/2022
ms.locfileid: "63781172"
---
# <a name="ipersistmessage--iunknown"></a>IPersistMessage : IUnknown

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Permet aux visionneuses de formulaire de gérer le stockage d’un formulaire et de passer des différents états.
  
|Propriété|Valeur|
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapiform.h  <br/> |
|Exposé par :  <br/> |Persister les objets de message  <br/> |
|Implémenté par :  <br/> |Objets de formulaires  <br/> |
|Appelé par :  <br/> |Visionneuses de formulaires  <br/> |
|Identificateur d’interface :  <br/> |IID_IPersistMessage  <br/> |
|Type de pointeur :  <br/> |LPPERSISTMESSAGE  <br/> |
   
## <a name="vtable-order"></a>Ordre des vtables

|Member|Description|
|:-----|:-----|
|[GetLastError](ipersistmessage-getlasterror.md) <br/> |Renvoie une [structure MAPIERROR](mapierror.md) qui contient des informations sur l’erreur précédente dans l’objet de formulaire. |
|[GetClassID](ipersistmessage-getclassid.md) <br/> |Renvoie un identificateur qui représente le serveur de formulaires qui peut gérer le formulaire. |
|[IsDirty](ipersistmessage-isdirty.md) <br/> |Recherche dans le formulaire les modifications apportées depuis le dernier sauvegarde. |
|[InitNew](ipersistmessage-initnew.md) <br/> |Initialise un nouveau message. |
|[Load](ipersistmessage-load.md) <br/> |Charge le formulaire pour un message spécifié. |
|[Save](ipersistmessage-save.md) <br/> |Enregistre un formulaire révisé dans le message à partir duquel il a été chargé ou créé. |
|[SaveCompleted](ipersistmessage-savecompleted.md) <br/> |Avertit le formulaire qu’une opération d’enregistrer a été effectuée. |
|[HandsOffMessage](ipersistmessage-handsoffmessage.md) <br/> |Fait en sorte que le formulaire libère son message actuel. |
   
## <a name="remarks"></a>Remarques

Tous les formulaires sont requis pour **implémenter l’interface IPersistMessage** . 
  
 **IPersistMessage** fonctionne de la même manière que l’interface OLE [IPersistStorage](https://msdn.microsoft.com/library/1c1a20fc-c101-4cbc-a7a6-30613aa387d7%28Office.15%29.aspx) . Pour plus d’informations, **voir les méthodes IPersistStorage** . 
  
## <a name="see-also"></a>Voir aussi



[Interfaces MAPI](mapi-interfaces.md)

