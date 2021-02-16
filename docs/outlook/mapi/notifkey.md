---
title: NOTIFKEY
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.NOTIFKEY
api_type:
- COM
ms.assetid: 031b7e18-59b2-445c-a747-348fda92f458
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: ab1586696a4b72aa9e88545c2069c3f8b5d22d72
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33429627"
---
# <a name="notifkey"></a>NOTIFKEY

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Identifie de manière unique une connexion entre un sink de conseil, une source de conseil et MAPI.
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapispi.h  <br/> |
   
```cpp
typedef struct
{
  ULONG cb;
  BYTE ab[MAPI_DIM];
} NOTIFKEY, FAR *LPNOTIFKEY;

```

## <a name="members"></a>Members

 **cb**
  
> Nombre d’octets dans le **membre ab.** 
    
 **ab**
  
> Tableau d’octets décrivant la clé de notification.
    
## <a name="remarks"></a>Remarques

Les [méthodes Subscribe](imapisupport-subscribe.md) et [Notify](imapisupport-notify.md) d’IMAPISupport utilisent la structure **NOTIFKEY** pour générer des notifications au réception de notifications approprié concernant la source de notification appropriée. [](imapisupportiunknown.md) 
  
Les fournisseurs de services génèrent des clés de notification lorsque leur méthode **Advise** est appelée et qu’ils souhaitent appeler **Subscribe** pour gérer l’inscription de la notification et l’envoi ultérieur de notifications. Une clé de notification peut être l’identificateur d’entrée de la source de notification ou tout autre élément d’identification tel qu’une constante. Par exemple, un fournisseur de magasins de messages peut utiliser le chemin d’accès d’un dossier comme clé de notification. 
  
La clé de notification doit fonctionner sur plusieurs processus. 
  
Les exigences d’étendue d’une clé de notification ressemblent à celles d’un identificateur d’entrée à long terme. Toutefois, contrairement à un identificateur d’entrée, une clé de notification doit être comparable au binaire. En règle générale, une clé de notification inclut une valeur **GUID** définie par le fournisseur de services, suivie d’autres informations spécifiques au fournisseur propres à l’objet. 
  
Pour une discussion sur l’utilisation de la structure **NOTIFKEY** pour gérer les connexions entre les réceptions de notification et les objets qui génèrent les notifications, voir Notification d’événement de [prise en charge.](supporting-event-notification.md) 
  
## <a name="see-also"></a>Voir aussi



[Structures MAPI](mapi-structures.md)

