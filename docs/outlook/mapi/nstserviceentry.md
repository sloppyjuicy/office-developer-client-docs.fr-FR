---
title: NSTServiceEntry
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 5ada6363-2406-4c0a-8326-a299a8bbefe1
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 96c04a242c477204ea1447fb78c31d189eeac59a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32280053"
---
# <a name="nstserviceentry"></a>NSTServiceEntry

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Fonction de point d'entrée de service de messagerie pour un fournisseur de magasin MAPI afin d'encapsuler un magasin local PST en tant que banque NST. 
  
## <a name="quick-info"></a>Informations rapides

|||
|:-----|:-----|
|Implémenté par :  <br/> |Fournisseur MAPI  <br/> |
|Appelé par :  <br/> |MAPI  <br/> |
   
```cpp
HRESULT NSTServiceEntry( 
    HINSTANCE hInstance,   
    LPMALLOC lpMalloc, 
    LPMAPISUP lpMAPISup, 
    ULONG ulUIParam, 
    ULONG ulFlags, 
    ULONG ulContext, 
    ULONG cValues, 
    LPSPropValue lpProps, 
    LPPROVIDERADMIN lpProviderAdmin, 
    LPMAPIERROR FAR * lppMapiError 
);
```

## <a name="parameters"></a>Paramètres

 **NSTServiceEntry** utilise le prototype de fonction **[MSGSERVICEENTRY](msgserviceentry.md)** . Pour plus d'informations sur ses paramètres, consultez la rubrique **[MSGSERVICEENTRY](msgserviceentry.md)**. 
  
## <a name="return-values"></a>Valeurs de retour

Pour plus d'informations sur les valeurs renvoyées, voir **[MSGSERVICEENTRY](msgserviceentry.md)**. 
  
## <a name="remarks"></a>Remarques

Lors de l'utilisation de **[GetProcAddress](https://msdn.microsoft.com/library/ms683212.aspx)** pour Rechercher l'adresse de cette fonction dans msmapi32. dll, spécifiez «NSTServiceEntry» comme nom de procédure. 
  
Pour utiliser l'API de réPlication, un fournisseur de banque MAPI doit d'abord ouvrir et envelopper un magasin local PST en appelant **[NSTServiceEntry](nstserviceentry.md)**. Le fournisseur peut ensuite utiliser les principales interfaces de l'API **[IOSTX](iostxiunknown.md)** et **[IPSTX](ipstxiunknown.md)** pour effectuer la réplication. 
  
Les notes suivantes s'appliquent à un magasin NST:
  
- Ne stockez pas d'informations dans la section profil global lors de l'implémentation d'un fournisseur MAPI qui utilise **NSTServiceEntry**. La section de profil global est partagée par de nombreux fournisseurs et les données stockées dans ce profil peuvent être remplacées. 
    
- Seuls les éléments avec des horodatages de modification existants reçoivent leurs tampons mis à jour lors de leur enregistrement. 
    
- La vérification des conflits ne se produit pas automatiquement lorsque des éléments sont enregistrés.
    
-  La détection des doublons n'a pas lieu lors de l'enregistrement des éléments. 
    
-  Le fichier représentant la version mise en cache du serveur est suivi de. Navisphere. 
    
- Pour obtenir un pointeur vers la section profil global, un service de messagerie appelle **[IMAPISupport:: OpenProfileSection](imapisupport-openprofilesection.md)** dans l'objet de prise en charge à l'aide de **pbNSTGlobalProfileSectionGuid** , comme indiqué ci-dessous: 
    
  ```
  #define  pbNSTGlobalProfileSectionGuid "\x85\xED\x14\x23\x9D\xF7\x42\x66\x8B\xF2\xFB\xD4\xA5\x21\x29\x41"
  ```

- Dans ce cas, l'objet de prise en charge du service de messagerie doit s'assurer que **IMAPISupport:: OpenProfileSection** renvoie la section de profil qui est identifiée par la propriété **[PR_SERVICE_UID](pidtagserviceuid-canonical-property.md)** dans la section profil par défaut. Pour obtenir cette section de profil, l'objet support peut ouvrir la section profil par défaut, extraire **PR_SERVICE_UID**et transmettre le résultat à **IMAPISupport:: OpenProfileSection** afin de récupérer la section de profil global appropriée. L'objet support retourne à son tour un pointeur vers cette section de profil global vers le service de messagerie. 
    
## <a name="see-also"></a>Voir aussi



[À propos de l’API de réplication](about-the-replication-api.md)

