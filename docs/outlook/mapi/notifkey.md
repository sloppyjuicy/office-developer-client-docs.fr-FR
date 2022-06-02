---
title: NOTIFKEY
description: Décrit la syntaxe, les membres et les remarques pour NOTIFKEY, qui identifie de façon unique une connexion entre un récepteur de conseils, une source de conseil et MAPI.
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
ms.openlocfilehash: 4830f25d26c37d26dcc8dbff00b20f2e8da190d5
ms.sourcegitcommit: 1b44c8f9eac3aedaf7fe7ec70c808fe8ed7d4b99
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/02/2022
ms.locfileid: "65852676"
---
# <a name="notifkey"></a>NOTIFKEY

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Identifie de façon unique une connexion entre un récepteur de conseils, une source de conseil et MAPI.
  
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
  
> Nombre d’octets dans le membre **ab** . 
    
 **Ab**
  
> Tableau d’octets décrivant la clé de notification.
    
## <a name="remarks"></a>Remarques

Les méthodes [Subscribe](imapisupport-subscribe.md) et [Notify](imapisupport-notify.md) [d’IMAPISupport](imapisupportiunknown.md) utilisent la structure **NOTIFKEY** pour générer des notifications au récepteur de conseils approprié sur la source de conseil appropriée. 
  
Les fournisseurs de services génèrent des clés de notification lorsque leur méthode **Advise** est appelée et qu’ils souhaitent appeler **Subscribe** pour gérer l’inscription des notifications et l’envoi ultérieur de notifications. Une clé de notification peut être l’identificateur d’entrée de la source de conseil ou tout autre élément d’identification tel qu’une constante. Par exemple, un fournisseur de magasin de messages peut utiliser le chemin d’accès d’un dossier comme clé de notification. 
  
La clé de notification doit fonctionner sur plusieurs processus. 
  
Les exigences d’étendue d’une clé de notification ressemblent à celles d’un identificateur d’entrée à long terme. Toutefois, contrairement à un identificateur d’entrée, une clé de notification doit être comparable binaire. En règle générale, une clé de notification inclut une valeur **GUID** définie par le fournisseur de services, suivie d’autres informations spécifiques au fournisseur propres à l’objet. 
  
Pour une discussion sur l’utilisation de la structure **NOTIFKEY** pour gérer les connexions entre les récepteurs de conseils et les objets qui génèrent les notifications, voir [Notification d’événement de prise en charge](supporting-event-notification.md). 
  
## <a name="see-also"></a>Voir aussi



[Structures MAPI](mapi-structures.md)

