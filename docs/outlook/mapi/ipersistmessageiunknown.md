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
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 7eb65bbae2fca6648c3a701dfa5c83c5bf297ec5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32309603"
---
# <a name="ipersistmessage--iunknown"></a>IPersistMessage : IUnknown

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Permet aux visionneuses de formulaires de gérer le stockage d'un formulaire et de passer d'un État à l'autre.
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |MAPIForm. h  <br/> |
|Exposé par:  <br/> |Conserver les objets message  <br/> |
|Implémenté par :  <br/> |Objets de formulaires  <br/> |
|Appelé par :  <br/> |Visionneuses de formulaires  <br/> |
|Identificateur de l'interface:  <br/> |IID_IPersistMessage  <br/> |
|Type de pointeur:  <br/> |LPPERSISTMESSAGE  <br/> |
   
## <a name="vtable-order"></a>Ordre vtable

|||
|:-----|:-----|
|[Généré](ipersistmessage-getlasterror.md) <br/> |Renvoie une structure [MAPIERROR](mapierror.md) qui contient des informations sur l'erreur précédente dans l'objet Form.  <br/> |
|[GetClassID](ipersistmessage-getclassid.md) <br/> |Renvoie un identificateur qui représente le serveur de formulaires qui peut gérer le formulaire.  <br/> |
|[IsDirty](ipersistmessage-isdirty.md) <br/> |Vérifie si le formulaire a été modifié depuis le dernier enregistrement.  <br/> |
|[InitNew](ipersistmessage-initnew.md) <br/> |Initialise un nouveau message.  <br/> |
|[Load](ipersistmessage-load.md) <br/> |Charge le formulaire pour un message spécifié.  <br/> |
|[Save](ipersistmessage-save.md) <br/> |RéEnregistre un formulaire révisé dans le message à partir duquel il a été chargé ou créé.  <br/> |
|[SaveCompleted](ipersistmessage-savecompleted.md) <br/> |Avertit le formulaire qu'une opération d'enregistrement a été effectuée.  <br/> |
|[HandsOffMessage](ipersistmessage-handsoffmessage.md) <br/> |Entraîne la libération du message actuel par le formulaire.  <br/> |
   
## <a name="remarks"></a>Remarques

Tous les formulaires sont requis pour implémenter l'interface **IPersistMessage** . 
  
 **IPersistMessage** fonctionne de la même manière que l'interface OLE [IPersistStorage](https://msdn.microsoft.com/library/1c1a20fc-c101-4cbc-a7a6-30613aa387d7%28Office.15%29.aspx) . Pour plus d'informations, consultez les méthodes **IPersistStorage** . 
  
## <a name="see-also"></a>Voir aussi



[Interfaces MAPI](mapi-interfaces.md)

