---
title: Construction d’identificateurs d’entrée
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: bc2a9116-948e-4da3-96b8-26d73bcd63c4
ms.openlocfilehash: 26cdbf3fcbb565c60567f543b08ce599854fb1af
ms.sourcegitcommit: 5ec1a8ec9fc1470266842599cb68ce626b5bf3a1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/06/2022
ms.locfileid: "66620827"
---
# <a name="constructing-entry-identifiers"></a>Construction d’identificateurs d’entrée

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Les identificateurs d’entrée sont construits avec la structure [ENTRYID](entryid.md) . La structure **ENTRYID** est composée d’un indicateur qui décrit les attributs de l’identificateur d’entrée et de l’identificateur d’entrée réel. 
  
## <a name="entryid-structure"></a>EntryID, structure

La structure **ENTRYID** est définie comme suit : 
  
```cpp
typedef struct
{
    BYTE        abFlags[4];
    BYTE        ab[MAPI_DIM];
}  ENTRYID, FAR *LPENTRYID;
 
```

MAPI_DIM est une constante définie dans le fichier d’en-tête MapiDefs.h. 
  
Le premier octet du membre **abFlags** de 4 octets décrit le type et l’utilisation de l’identificateur d’entrée et peut avoir les valeurs suivantes : 
  
- MAPI_NOTRECIP : indique que l’identificateur d’entrée ne peut pas être utilisé comme destinataire sur un message.
    
- MAPI_NOTRESERVED : indique que d’autres utilisateurs ne peuvent pas accéder à l’identificateur d’entrée.
    
- MAPI_NOW : indique que l’identificateur d’entrée ne peut pas être utilisé à d’autres moments.
    
- MAPI_SHORTTERM : indique que l’identificateur d’entrée est à court terme. Toutes les autres valeurs de cet octet doivent être définies, sauf si d’autres utilisations de l’identificateur d’entrée sont autorisées.
    
- MAPI_THISSESSION : indique que l’identificateur d’entrée ne peut pas être utilisé sur d’autres sessions.
    
- MAPI_NOTRESERVED : indique que l’identificateur d’entrée peut être utilisé par d’autres fournisseurs de services pour d’autres objets.
    
Le **membre ab** des identificateurs d’entrée créés par les fournisseurs de carnet d’adresses et de magasins de messages est composé de deux éléments : une structure [MAPIUID](mapiuid.md) de 16 octets qui identifie le fournisseur de services et une pièce pour identifier l’objet. **MAPIUID** est une structure qui contient un identificateur global unique, ou GUID. Un GUID est un identificateur indépendant de l’ordre d’octet qui peut être créé à l’aide de l’outil Microsoft Visual Studio *Create GUID**. 
  
Un fournisseur de services inscrit sa structure **MAPIUID** auprès de MAPI pendant le processus d’ouverture de session dans un appel à la méthode [IMAPISupport::SetProviderUID](imapisupport-setprovideruid.md) . Lorsqu’un client appelle une méthode **OpenEntry** pour accéder à un objet, MAPI utilise la structure **MAPIUID** pour déterminer quel fournisseur de services peut fournir cet accès. Les fournisseurs de services doivent utiliser la même structure **MAPIUID** pour toutes les versions de leur DLL. Cela permet aux clients avec la version la plus récente de répondre aux messages envoyés et enregistrés avec l’ancienne version. 
  
Le reste du membre **ab** après le **MAPIUID** de 16 octets contient des données binaires spécifiques au fournisseur de services pour identifier des objets particuliers. Il n’existe aucune taille fixe pour cette partie de l’identificateur d’entrée. Il peut être n’importe quelle taille, dans la raison. Un fournisseur de services inclut généralement les informations suivantes dans cette partie de ses identificateurs d’entrée : 
  
- Informations sur la version — Étant donné qu’il est courant pour un fournisseur de services de modifier le format de ses identificateurs d’entrée de version en version, le stockage des informations de version permet de déterminer rapidement comment déchiffrer n’importe quel identificateur d’entrée.
    
- Informations d’emplacement : les informations d’emplacement sont des données qui donnent à un fournisseur de services un indicateur de la façon de localiser l’objet représenté par l’identificateur d’entrée. Par exemple, un fournisseur de services peut stocker le décalage de disque pour le dernier emplacement dans un fichier de données que l’objet a été stocké. Étant donné que ce type d’informations peut changer au fil du temps, les fournisseurs de services doivent fournir plusieurs façons de localiser des objets dans leurs identificateurs d’entrée.
    
Bien que les fournisseurs de services puissent recycler leurs identificateurs d’entrée, ils doivent éviter cette pratique. S’il est nécessaire de réutiliser un identificateur d’entrée, les fournisseurs de services doivent faire le délai qui s’écoule entre l’utilisation initiale et la réutilisation aussi longtemps que possible. En outre, l’identificateur d’entrée doit être réattribué à un autre objet du même type. Autrement dit, un identificateur d’entrée particulier ne doit pas être associé d’abord à un message, puis à un dossier.
  
## <a name="see-also"></a>Voir aussi



[Identificateurs d’entrée MAPI](mapi-entry-identifiers.md)

