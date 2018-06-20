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
ms.openlocfilehash: b5902c25197c2ae5790e654a8f29227e107b4a72
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19784912"
---
# <a name="nstserviceentry"></a>NSTServiceEntry

  
  
**S’applique à**: Outlook 
  
Fonction de point d’entrée de service de message pour une MAPI stocker le fournisseur à utiliser un magasin local PST comme une banque NST. 
  
## <a name="quick-info"></a>Informations rapides

|||
|:-----|:-----|
|Implémentée par :  <br/> |Fournisseur MAPI  <br/> |
|Appelée par :  <br/> |MAPI  <br/> |
   
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

 **NSTServiceEntry** utilise le prototype de fonction **[MSGSERVICEENTRY](msgserviceentry.md)** . Pour plus d’informations sur ses paramètres, voir **[MSGSERVICEENTRY](msgserviceentry.md)**. 
  
## <a name="return-values"></a>Valeurs de retour

Pour plus d’informations sur les valeurs de retour, voir **[MSGSERVICEENTRY](msgserviceentry.md)**. 
  
## <a name="remarks"></a>Remarques

Lorsque vous utilisez **[GetProcAddress](http://msdn.microsoft.com/en-us/library/ms683212.aspx)** pour rechercher l’adresse de cette fonction dans msmapi32.dll, spécifiez « NSTServiceEntry » comme nom de la procédure. 
  
Pour utiliser l’API de réplication, un fournisseur de banque MAPI doit tout d’abord ouvrir et renvoyer un magasin local PST en appelant **[NSTServiceEntry](nstserviceentry.md)**. Le fournisseur peut utiliser ensuite les interfaces principales des API, **[IOSTX](iostxiunknown.md)** et **[IPSTX](ipstxiunknown.md)**, pour effectuer la réplication. 
  
Les notes suivantes s’appliquent à un magasin de NST :
  
- Ne stockez pas les informations dans la section profil global lors de l’implémentation d’un fournisseur MAPI qui utilise **NSTServiceEntry**. La section profil global est partagée par tous les fournisseurs et les données stockées dans ce profil peuvent être remplacées. 
    
- Uniquement les éléments dont les horodatages modification existant obtenir leurs cachets de mise à jour lorsqu’ils sont enregistrés. 
    
- Vérification des conflits ne produit pas automatiquement lorsque des éléments sont enregistrés.
    
-  Détection des doublons ne se produit pas lorsque des éléments sont enregistrés. 
    
-  Le fichier représentant la version en cache du serveur est ajouté avec. NST. 
    
- Pour obtenir un pointeur vers la section profil global, un service de message appelle **[IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md)** dans l’objet de prise en charge à l’aide de **pbNSTGlobalProfileSectionGuid** tels que définis ci-dessous : 
    
  ```
  #define  pbNSTGlobalProfileSectionGuid "\x85\xED\x14\x23\x9D\xF7\x42\x66\x8B\xF2\xFB\xD4\xA5\x21\x29\x41"
  ```

- Dans ce cas, l’objet de prise en charge du service de message doit garantir que **IMAPISupport::OpenProfileSection** retourne la section profil qui est identifiée par la propriété **[PR_SERVICE_UID](pidtagserviceuid-canonical-property.md)** dans la section de profil par défaut. Pour obtenir cette section de profil, l’objet de prise en charge peut ouvrir la section de profil par défaut, récupérez **PR_SERVICE_UID**et transmettre le résultat à **IMAPISupport::OpenProfileSection** pour récupérer la section profil global. L’objet de prise en charge retourne à son tour un pointeur vers cette section de profil global pour le service de message. 
    
## <a name="see-also"></a>Voir aussi



[À propos de l’API de réplication](about-the-replication-api.md)

