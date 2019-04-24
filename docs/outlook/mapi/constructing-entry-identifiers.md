---
title: Construction d'identificateurs d'entrée
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: bc2a9116-948e-4da3-96b8-26d73bcd63c4
description: 'Dernière modification : 23 juillet 2011'
ms.openlocfilehash: 8d48c2584fa5b7e862102e401ea8165821607f77
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32335090"
---
# <a name="constructing-entry-identifiers"></a>Construction d'identificateurs d'entrée

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Les identificateurs d'entrée sont créés à l'aide de la structure [EntryID](entryid.md) . La structure **EntryID** est composée d'un indicateur qui décrit les attributs de l'identificateur d'entrée et de l'identificateur d'entrée réel. 
  
## <a name="entryid-structure"></a>Structure ENTRYID

La structure **EntryID** est définie comme suit: 
  
```cpp
typedef struct
{
    BYTE        abFlags[4];
    BYTE        ab[MAPI_DIM];
}  ENTRYID, FAR *LPENTRYID;
 
```

MAPI_DIM est une constante qui est définie dans le fichier d'en-tête MapiDefs. h. 
  
Le premier octet du membre **abFlags** 4 octets décrit le type et l'utilisation de l'identificateur d'entrée et peut avoir les valeurs suivantes: 
  
- MAPI_NOTRECI — indique que l'identificateur d'entrée ne peut pas être utilisé comme destinataire sur un message.
    
- MAPI_NOTRESERVED: indique que les autres utilisateurs ne peuvent pas accéder à l'identificateur d'entrée.
    
- MAPI_NOW: indique que l'identificateur d'entrée ne peut pas être utilisé à d'autres moments.
    
- MAPI_SHORTTERM: indique que l'identificateur d'entrée est à court terme. Toutes les autres valeurs de cet octet doivent être définies sauf si les autres utilisations de l'identificateur d'entrée sont autorisées.
    
- MAPI_THISSESSION: indique que l'identificateur d'entrée ne peut pas être utilisé pour d'autres sessions.
    
- MAPI_NOTRESERVED: indique que l'identificateur d'entrée peut être utilisé par d'autres fournisseurs de services pour d'autres objets.
    
Le membre **AB** des identificateurs d'entrée créés par les fournisseurs de carnet d'adresses et de banque de messages est composé de deux éléments: une structure [MAPIUID](mapiuid.md) à 16 octets qui identifie le fournisseur de services, ainsi qu'un élément permettant d'identifier l'objet. **MAPIUID** est une structure qui contient un identificateur global unique, ou GUID. Un GUID est un identificateur indépendant de l'ordre des octets qui peut être créé à l'aide de l'outil de*création de GUID** de Microsoft Visual Studio. 
  
Un fournisseur de services enregistre sa structure **MAPIUID** avec MAPI pendant le processus d'ouverture de session dans un appel à la méthode [IMAPISupport:: SetProviderUID](imapisupport-setprovideruid.md) . Lorsqu'un client appelle une méthode **OpenEntry** pour accéder à un objet, MAPI utilise la structure **MAPIUID** pour déterminer le fournisseur de services qui peut fournir cet accès. Les fournisseurs de services doivent utiliser la même structure **MAPIUID** pour toutes les versions de leur dll. Cela permet aux clients disposant de la version plus récente de répondre aux messages envoyés et enregistrés avec l'ancienne version. 
  
Le reste du membre **AB** après l' **MAPIUID** de 16 octets contient des données binaires spécifiques aux fournisseurs de services pour l'identification d'objets particuliers. Il n'existe aucune taille fixe pour cette partie de l'identificateur d'entrée. Il peut être de n'importe quelle taille, dans la mesure du possible. Un fournisseur de services inclut généralement les informations suivantes dans cette partie de ses identificateurs d'entrée: 
  
- Informations sur la version: étant donné qu'il est courant pour un fournisseur de services de modifier le format de ses identificateurs d'entrée de version à version, le stockage des informations de version permet de déterminer rapidement le déchiffrement de n'importe quel identificateur d'entrée.
    
- Informations d'emplacement: les informations d'emplacement sont des données qui donnent à un fournisseur de services un indicateur de la localisation de l'objet représenté par l'identificateur d'entrée. Par exemple, un fournisseur de services peut stocker le décalage de disque pour la dernière place d'un fichier de données dans lequel l'objet a été stocké. Étant donné que ce type d'informations peut changer au fil du temps, les fournisseurs de services doivent fournir plusieurs méthodes pour rechercher des objets dans leurs identificateurs d'entrée.
    
Bien que les fournisseurs de services puissent recycler leurs identificateurs d'entrée, ils doivent éviter cette pratique. S'il est nécessaire de réutiliser un identificateur d'entrée, les fournisseurs de services doivent prendre la période qui s'écoule entre l'utilisation initiale et la réutilisation aussi longtemps que possible. De plus, l'identificateur d'entrée doit être réattribué à un autre objet du même type. Autrement dit, un identificateur d'entrée particulier ne doit pas être associé d'abord à un message, puis à un dossier.
  
## <a name="see-also"></a>Voir aussi



[Identificateurs d'entrée MAPI](mapi-entry-identifiers.md)

