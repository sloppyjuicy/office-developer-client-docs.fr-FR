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
  
Identifie de manière unique une connexion entre un récepteur de notification, une source de notification et MAPI.
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapispi. h  <br/> |
   
```cpp
typedef struct
{
  ULONG cb;
  BYTE ab[MAPI_DIM];
} NOTIFKEY, FAR *LPNOTIFKEY;

```

## <a name="members"></a>Members

 **cb**
  
> Nombre d'octets dans le membre **AB** . 
    
 **opér**
  
> Tableau d'octets qui décrivent la clé de notification.
    
## <a name="remarks"></a>Remarques

Les méthodes [subscribe](imapisupport-subscribe.md) et [Notify](imapisupport-notify.md) de [IMAPISupport](imapisupportiunknown.md) utilisent la structure **NOTIFKEY** pour générer des notifications au récepteur de notification approprié concernant la source de notification appropriée. 
  
Les fournisseurs de services génèrent des clés de notification lorsque leur méthode de **Conseil** est appelée et qu'ils veulent appeler l' **abonnement** pour gérer l'inscription des notifications et l'envoi ultérieur de notifications. Une clé de notification peut être l'identificateur d'entrée de la source de notification ou il peut s'agir d'un autre élément d'identification tel qu'une constante. Par exemple, un fournisseur de banque de messages peut utiliser le chemin d'accès d'un dossier comme clé de notification. 
  
La clé de notification doit fonctionner sur plusieurs processus. 
  
Les exigences d'étendue pour une clé de notification ressemblent à celles d'un identificateur d'entrée à long terme. Toutefois, contrairement à un identificateur d'entrée, une clé de notification doit être comparable au format binaire. En règle générale, une clé de notification inclut une valeur **GUID** définie par le fournisseur de services, suivie d'autres informations propres au fournisseur, propres à l'objet. 
  
Pour plus d'informations sur l'utilisation de la structure **NOTIFKEY** pour gérer les connexions entre les récepteurs de notification et les objets qui génèrent les notifications, consultez la rubrique [prise en charge](supporting-event-notification.md)de la notification d'événement. 
  
## <a name="see-also"></a>Voir aussi



[Structures MAPI](mapi-structures.md)

