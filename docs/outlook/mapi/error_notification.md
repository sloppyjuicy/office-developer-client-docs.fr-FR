---
title: ERROR_NOTIFICATION
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.ERROR_NOTIFICATION
api_type:
- COM
ms.assetid: 6c5bb383-f8e2-4d79-bcf2-aa86c130e8b1
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 86fe4b0a1a7521c310788505b99f53bc8657de75
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19783266"
---
# <a name="errornotification"></a>ERROR_NOTIFICATION

  
  
**S’applique à**: Outlook 
  
Décrit les informations qui sont associées à une erreur critique. Cela entraîne une notification d’erreur à générer. 
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapidefs.h  <br/> |
   
```cpp
typedef struct _ERROR_NOTIFICATION
{
  ULONG cbEntryID;
  LPENTRYID lpEntryID;
  SCODE scode;
  ULONG ulFlags;
  LPMAPIERROR lpMAPIError;
} ERROR_NOTIFICATION;
```

## <a name="members"></a>Membres

 **cbEntryID**
  
> Nombre d’octets de l’identificateur d’entrée désignés par **lpEntryID**. 
    
 **lpEntryID**
  
> Pointeur vers l’identificateur d’entrée de l’objet qui provoque l’erreur.
    
 **SCODE**
  
> Valeur d’erreur pour l’erreur critique. 
    
 **ulFlags**
  
> Masque de bits d’indicateurs utilisés pour désigner le format du texte vers laquelle pointe le membre **lpszError** dans la structure désigné par **lpMAPIError**. Vous pouvez définir l’indicateur suivant :
    
MAPI_UNICODE 
  
> Les chaînes passée sont au format Unicode. Si l’indicateur MAPI_UNICODE n’est pas définie, les chaînes sont au format ANSI.
    
 **lpMAPIError**
  
> Pointeur vers une structure [MAPIERROR](mapierror.md) décrivant l’erreur. 
    
## <a name="remarks"></a>Remarques

La structure **ERROR_NOTIFICATION** est un des membres de l’union de structures inclus dans le membre **info** de la structure de [NOTIFICATION](notification.md) . Lorsque le membre **info** d’une structure **NOTIFICATION** contient une structure **ERROR_NOTIFICATION** , le membre **ulEventType** de la structure de **NOTIFICATION** est défini sur _fnevCriticalError_.
  
La valeur du membre **cbEntryID** et le membre **lpEntryID** peut être NULL. 
  
Pour plus d’informations sur la notification, consultez les rubriques décrites dans le tableau suivant.
  
|**Rubrique**|**Description**|
|:-----|:-----|
|[Notification d’événement MAPI](event-notification-in-mapi.md) <br/> |Vue d’ensemble des notifications et les événements de notification.  <br/> |
|[Gérer les Notifications](handling-notifications.md) <br/> |Étude de la façon dont les clients doivent gérer les notifications.  <br/> |
|[Prise en charge de la Notification d’événement](supporting-event-notification.md) <br/> |Étude de comment les fournisseurs de services peuvent utiliser la méthode **IMAPISupport** pour générer des notifications.  <br/> |
   
## <a name="see-also"></a>Voir aussi



[MAPIERROR](mapierror.md)
  
[Notification](notification.md)


[Structures MAPI](mapi-structures.md)

