---
title: NOTIFKEY
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.NOTIFKEY
api_type:
- COM
ms.assetid: 031b7e18-59b2-445c-a747-348fda92f458
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 85956244017af9491988dd08e4531afdfbd3943d
ms.sourcegitcommit: a355e6b8898e9a1d66ca1bc808fe106e78dcb68f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2022
ms.locfileid: "63723755"
---
# <a name="notifkey"></a>NOTIFKEY

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Identifie de manière unique une connexion entre un sink de conseil, une source de conseil et MAPI.
  
|Propriété |Valeur |
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
  
> Nombre d’octets dans le **membre ab** . 
    
 **ab**
  
> Tableau d’octets décrivant la clé de notification.
    
## <a name="remarks"></a>Remarques

Les [méthodes Subscribe](imapisupport-subscribe.md) et [Notify](imapisupport-notify.md) [d’IMAPISupport](imapisupportiunknown.md) utilisent la structure **NOTIFKEY** pour générer des notifications au réception de notifications approprié concernant la source de notification appropriée. 
  
Les fournisseurs de services génèrent des clés de notification lorsque leur méthode **Advise** est appelée et qu’ils souhaitent appeler **Subscribe** pour gérer l’inscription de la notification et l’envoi ultérieur de notifications. Une clé de notification peut être l’identificateur d’entrée de la source de notification ou tout autre élément d’identification tel qu’une constante. Par exemple, un fournisseur de magasins de messages peut utiliser le chemin d’accès d’un dossier comme clé de notification. 
  
La clé de notification doit fonctionner sur plusieurs processus. 
  
Les exigences d’étendue d’une clé de notification ressemblent à celles d’un identificateur d’entrée à long terme. Toutefois, contrairement à un identificateur d’entrée, une clé de notification doit être comparable au binaire. En règle générale, une clé de notification inclut une valeur **GUID** définie par le fournisseur de services, suivie d’autres informations spécifiques au fournisseur propres à l’objet. 
  
Pour une discussion sur l’utilisation de la structure **NOTIFKEY** pour gérer les connexions entre les réceptions de notification et les objets qui génèrent les notifications, voir Notification d’événement de [prise en charge](supporting-event-notification.md). 
  
## <a name="see-also"></a>Voir aussi



[Structures MAPI](mapi-structures.md)

