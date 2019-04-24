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
ms.openlocfilehash: f8d4fb6b8cd7ad0ebf1e7660a0f3c0602274fa10
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32335734"
---
# <a name="errornotification"></a>ERROR_NOTIFICATION

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Décrit les informations relatives à une erreur critique. Cela entraîne la génération d'une notification d'erreur. 
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapidefs. h  <br/> |
   
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

## <a name="members"></a>Members

 **cbEntryID**
  
> Nombre d'octets dans l'identificateur d'entrée pointé par **lpEntryID**. 
    
 **lpEntryID**
  
> Pointeur vers l'identificateur d'entrée de l'objet à l'origine de l'erreur.
    
 **SCODE**
  
> Valeur d'erreur pour l'erreur critique. 
    
 **ulFlags**
  
> Masque de des indicateurs utilisé pour désigner le format du texte pointé par le membre **lpszError** dans la structure vers laquelle pointe le **lpMAPIError**. L'indicateur suivant peut être défini:
    
MAPI_UNICODE 
  
> Les chaînes transmises sont au format Unicode. Si l'indicateur MAPI_UNICODE n'est pas défini, les chaînes sont au format ANSI.
    
 **lpMAPIError**
  
> Pointeur vers une structure [MAPIERROR](mapierror.md) décrivant l'erreur. 
    
## <a name="remarks"></a>Remarques

La structure **ERROR_NOTIFICATION** est l'un des membres de l'Union des structures incluses dans le membre **info** de la structure de [notification](notification.md) . Lorsque le membre **info** d'une structure de **notification** contient une structure **ERROR_NOTIFICATION** , le membre **ulEventType** de la structure de **notification** est défini sur _fnevCriticalError_.
  
La valeur du membre **cbEntryID** et du membre **LPENTRYID** peut être null. 
  
Pour plus d'informations sur la notification, reportez-vous aux rubriques décrites dans le tableau suivant.
  
|**Rubrique**|**Description**|
|:-----|:-----|
|[Notification d'événement dans MAPI](event-notification-in-mapi.md) <br/> |Vue d'ensemble générale des événements de notification et de notification.  <br/> |
|[Gestion des notifications](handling-notifications.md) <br/> |Présentation de la façon dont les clients doivent gérer les notifications.  <br/> |
|[Notification d'événement de prise en charge](supporting-event-notification.md) <br/> |Présentation de la façon dont les fournisseurs de services peuvent utiliser la méthode **IMAPISupport** pour générer des notifications.  <br/> |
   
## <a name="see-also"></a>Voir aussi



[MAPIERROR](mapierror.md)
  
[Notification](notification.md)


[Structures MAPI](mapi-structures.md)

