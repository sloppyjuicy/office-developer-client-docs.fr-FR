---
title: NSTServiceEntry
description: NSTServiceEntry est la fonction de point d’entrée du service de message permettant à un fournisseur de magasin MAPI d’encapsuler un magasin local basé sur PST en tant que magasin NST.
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 5ada6363-2406-4c0a-8326-a299a8bbefe1
ms.openlocfilehash: 98d7f4d84611e04916216bd31c7438220752d5d3
ms.sourcegitcommit: 1b44c8f9eac3aedaf7fe7ec70c808fe8ed7d4b99
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/02/2022
ms.locfileid: "65854720"
---
# <a name="nstserviceentry"></a>NSTServiceEntry

**S’applique à** : Outlook 2013 | Outlook 2016
  
Fonction de point d’entrée du service de message pour qu’un fournisseur de magasin MAPI encapsule un magasin local basé sur PST en tant que magasin NST.
  
## <a name="quick-info"></a>Informations rapides

|Propriété|Valeur|
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

**NSTServiceEntry** utilise le prototype de fonction **[MSGSERVICEENTRY](msgserviceentry.md)** . Pour plus d’informations sur ses paramètres, consultez **[MSGSERVICEENTRY](msgserviceentry.md)**.
  
## <a name="return-values"></a>Valeurs de retour

Pour plus d’informations sur les valeurs de retour, consultez **[MSGSERVICEENTRY](msgserviceentry.md)**.
  
## <a name="remarks"></a>Remarques

Lorsque **[vous utilisez GetProcAddress](https://msdn.microsoft.com/library/ms683212.aspx)** pour rechercher l’adresse de cette fonction dans msmapi32.dll, spécifiez « NSTServiceEntry » comme nom de procédure.
  
Pour utiliser l’API de réplication, un fournisseur de magasin MAPI doit d’abord ouvrir et encapsuler un magasin local basé sur **[PST en appelant NSTServiceEntry](nstserviceentry.md)**. Le fournisseur peut ensuite utiliser les interfaces principales de l’API, **[IOSTX](iostxiunknown.md)** et **[IPSTX](ipstxiunknown.md)**, pour effectuer la réplication.
  
Les remarques suivantes s’appliquent à un magasin NST :
  
- Ne stockez aucune information dans la section profil global lors de l’implémentation d’un fournisseur MAPI qui utilise **NSTServiceEntry**. La section profil global est partagée par de nombreux fournisseurs et les données stockées dans ce profil peuvent être remplacées.

- Seuls les éléments avec des horodatages de modification existants sont mis à jour lorsqu’ils sont enregistrés.

- La vérification des conflits ne se produit pas automatiquement lorsque des éléments sont enregistrés.

- La détection des doublons ne se produit pas lorsque des éléments sont enregistrés.

- Le fichier représentant la version mise en cache du serveur est ajouté avec . NST.

- Pour obtenir un pointeur vers la section de profil global, un service de message appelle **[IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md)** dans l’objet de support à l’aide de **pbNSTGlobalProfileSectionGuid** comme défini ci-dessous :

  ```
  #define  pbNSTGlobalProfileSectionGuid "\x85\xED\x14\x23\x9D\xF7\x42\x66\x8B\xF2\xFB\xD4\xA5\x21\x29\x41"
  ```

- Dans ce cas, l’objet de support du service de message doit s’assurer **qu’IMAPISupport::OpenProfileSection** retourne la section de profil identifiée par la propriété **[PR_SERVICE_UID](pidtagserviceuid-canonical-property.md)** dans la section de profil par défaut. Pour obtenir cette section de profil, l’objet de support peut ouvrir la section de profil par défaut, récupérer **PR_SERVICE_UID** et transmettre le résultat à **IMAPISupport::OpenProfileSection** pour récupérer la section de profil global correcte. L’objet de support retourne à son tour un pointeur vers cette section de profil global vers le service de message.

## <a name="see-also"></a>Voir aussi

[À propos de l’API de réplication](about-the-replication-api.md)
