---
title: ERROR_NOTIFICATION
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.ERROR_NOTIFICATION
api_type:
- COM
ms.assetid: 6c5bb383-f8e2-4d79-bcf2-aa86c130e8b1
description: Décrit les informations liées à une erreur critique. Une notification d’erreur est alors générée.
ms.openlocfilehash: 628ab3cb994fffb21275315cfbd7d1e83e3a34c8
ms.sourcegitcommit: 0a067f44281eddabff15fff565fb80eaa543b660
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/23/2022
ms.locfileid: "63762143"
---
# <a name="error_notification"></a>ERROR_NOTIFICATION

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Décrit les informations liées à une erreur critique. Une notification d’erreur est alors générée. 
  
|Propriété |Valeur |
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

## <a name="members"></a>Members

 **cbEntryID**
  
> Nombre d’octets dans l’identificateur d’entrée pointé par **lpEntryID**. 
    
 **lpEntryID**
  
> Pointeur vers l’identificateur d’entrée de l’objet à l’origine de l’erreur.
    
 **scode**
  
> Valeur d’erreur pour l’erreur critique. 
    
 **ulFlags**
  
> Masque de bits d’indicateurs utilisé pour désigner le format du texte pointé par le membre **lpszError** dans la structure pointée par **lpMAPIError**. L’indicateur suivant peut être définie :
    
MAPI_UNICODE 
  
> Les chaînes transmises sont au format Unicode. Si l’MAPI_UNICODE n’est pas définie, les chaînes sont au format ANSI.
    
 **lpMAPIError**
  
> Pointeur vers une structure [MAPIERROR](mapierror.md) décrivant l’erreur. 
    
## <a name="remarks"></a>Remarques

La **ERROR_NOTIFICATION** structure est l’un des membres de l’union des structures incluses dans le membre **d’informations** de la structure [NOTIFICATION](notification.md) . Lorsque le **membre d’informations** d’une structure **NOTIFICATION** contient une structure **ERROR_NOTIFICATION** , le membre **ulEventType** de la structure **NOTIFICATION** est définie sur  _fnevCriticalError_.
  
La valeur du **membre cbEntryID** et du membre **lpEntryID** peut être NULL. 
  
Pour plus d’informations sur la notification, voir les rubriques décrites dans le tableau suivant.
  
|**Rubrique**|**Description**|
|:-----|:-----|
|[Notification d’événement dans MAPI](event-notification-in-mapi.md) <br/> |Vue d’ensemble des événements de notification et de notification. |
|[Gestion des notifications](handling-notifications.md) <br/> |Discussion sur la façon dont les clients doivent gérer les notifications. |
|[Prise en charge des notifications d’événement](supporting-event-notification.md) <br/> |Discussion sur la façon dont les fournisseurs de services peuvent utiliser la méthode **IMAPISupport** pour générer des notifications. |
   
## <a name="see-also"></a>Voir aussi



[MAPIERROR](mapierror.md)
  
[Notification](notification.md)


[Structures MAPI](mapi-structures.md)

