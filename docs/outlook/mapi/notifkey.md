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
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 3c480c420753b2da6c57b3961589d5c2e2e8022a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19784921"
---
# <a name="notifkey"></a>NOTIFKEY

  
  
**S’applique à**: Outlook 
  
Identifie de manière unique une connexion entre un récepteur de notifications, une source de notifications et MAPI.
  
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

## <a name="members"></a>Membres

 **cb**
  
> Nombre d’octets dans le membre de **Carnet d’adresses** . 
    
 **Carnet d’adresses**
  
> Tableau d’octets décrivant la clé de notification.
    
## <a name="remarks"></a>Remarques

Les méthodes [Subscribe](imapisupport-subscribe.md) et [notifier](imapisupport-notify.md) de [IMAPISupport](imapisupportiunknown.md) permet de générer des notifications pour le récepteur de notifications appropriées sur la source advise appropriée la structure **NOTIFKEY** . 
  
Fournisseurs de services de génèrent des clés de notification lorsque leur méthode **Advise** est appelée et qu’ils souhaitent **s’abonner** pour gérer l’inscription de notification et l’envoi suivants de notifications d’appel. Une clé de notification peut être l’identificateur d’entrée de la source advise ou elle peut être n’importe quel autre élément identification comme une constante. Par exemple, un fournisseur de magasin de message peut utiliser le chemin d’accès d’un dossier en tant que sa clé de notification. 
  
La clé de notification devrait fonctionner sur plusieurs processus. 
  
Les exigences de l’étendue d’une clé de notification ressemblent à celles d’un identificateur d’entrée à long terme. Toutefois, contrairement à un identificateur d’entrée, une clé de notification doit être binaire comparable. En règle générale, une clé de notification inclut une valeur **GUID** définie par le fournisseur de suivi d’autres informations spécifiques au fournisseur uniques à l’objet. 
  
Pour une description de l’utilisation de la structure **NOTIFKEY** pour gérer les connexions entre les récepteurs de notifications et les objets qui génèrent des notifications, voir [Prise en charge de Notification d’événement](supporting-event-notification.md). 
  
## <a name="see-also"></a>Voir aussi



[Structures MAPI](mapi-structures.md)

