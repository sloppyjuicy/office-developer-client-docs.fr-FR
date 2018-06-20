---
title: Construction d’identificateurs d’entrée
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: bc2a9116-948e-4da3-96b8-26d73bcd63c4
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: 1d38c0ac7ddbd24123dd51d7315644f3ad786d15
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19783053"
---
# <a name="constructing-entry-identifiers"></a>Construction d’identificateurs d’entrée

  
  
**S’applique à**: Outlook 
  
Identificateurs d’entrée sont construits avec la structure [ENTRYID](entryid.md) . La structure de la **propriété ENTRYID** est composée d’un indicateur qui décrit les attributs de l’identificateur d’entrée et de l’identificateur d’entrée réelle. 
  
## <a name="entryid-structure"></a>Propriété ENTRYID Structure

La structure de la **propriété ENTRYID** est définie comme suit : 
  
```cpp
typedef struct
{
    BYTE        abFlags[4];
    BYTE        ab[MAPI_DIM];
}  ENTRYID, FAR *LPENTRYID;
 
```

MAPI_DIM est une constante qui est définie dans le fichier d’en-tête MapiDefs.h. 
  
Le premier octet du membre 4 octets **abFlags** décrit le type et utilisation de l’identificateur d’entrée et peut avoir les valeurs suivantes : 
  
- MAPI_NOTRECI — Indique l’identificateur d’entrée ne peut pas être utilisé en tant que destinataire d’un message.
    
- MAPI_NOTRESERVED — Indique que les autres utilisateurs ne peuvent pas accéder à l’identificateur d’entrée.
    
- MAPI_NOW — Indique que l’identificateur d’entrée ne peut pas être utilisé à d’autres moments.
    
- MAPI_SHORTTERM — Indique que l’identificateur d’entrée est à court terme. Toutes les autres valeurs dans cet octet doivent être définies à moins que les autres utilisations de l’identificateur d’entrée sont autorisées.
    
- MAPI_THISSESSION — Indique que l’identificateur d’entrée ne peut pas être utilisé sur d’autres sessions.
    
- MAPI_NOTRESERVED — Indique que l’identificateur d’entrée peut être utilisée par les autres fournisseurs de services pour d’autres objets.
    
Le membre de **Carnet d’adresses** d’identificateurs d’entrée qui est créé par les fournisseurs de banque de messages et du carnet d’adresse est composé de deux parties : une structure [MAPIUID](mapiuid.md) de 16 octets qui identifie le fournisseur de services et un élément pour identifier l’objet. **MAPIUID** est une structure qui contient un identificateur global unique, ou le GUID. Un GUID est un identificateur indépendant de l’ordre octets qui peut être créé à l’aide de Microsoft Visual Studio*Create GUID** outil. 
  
Un fournisseur de services enregistre sa structure **MAPIUID** MAPI au cours du processus d’ouverture de session dans un appel à la méthode [IMAPISupport::SetProviderUID](imapisupport-setprovideruid.md) . Lorsqu’un client appelle une méthode **OpenEntry** pour accéder à un objet, MAPI utilise la structure **MAPIUID** pour déterminer quel service fournisseur peut fournir cet accès. Fournisseurs de services doivent utiliser la même structure **MAPIUID** pour toutes les versions de leur DLL. Cela permet aux clients avec la version la plus récente répondre aux messages envoyés et enregistré avec la version antérieure. 
  
Le reste du membre **ab** après le 16 octets **MAPIUID** contient des données binaires spécifique au fournisseur de service pour identifier des objets particulières. Il n’existe aucune taille fixe pour cette partie de l’identificateur d’entrée. Il peut être n’importe quelle taille, dans le motif. En règle générale, un fournisseur de services comprend les informations suivantes dans cette partie de son identificateur d’entrée : 
  
- Informations de version, car il est courant pour un fournisseur de services modifier le format de son identificateur d’entrée pour chaque version, le stockage des informations de version permet de déterminer rapidement comment déchiffrer un identificateur d’entrée.
    
- Informations d’emplacement, informations d’emplacement sont des données qui permet à un fournisseur de services indique comment localiser l’objet représenté par l’identificateur d’entrée. Par exemple, un fournisseur de services peut stocker le disque décalage du dernier lieu dans un fichier de données que l’objet a été enregistré. Car ce type d’informations peut changer au fil du temps, les fournisseurs de services doivent fournir plusieurs façons pour localiser des objets dans leurs identificateurs d’entrée.
    
Bien que les fournisseurs de services peuvent recycler leurs identificateurs d’entrée, ils doivent éviter cette pratique. S’il est nécessaire réutiliser un identificateur d’entrée, les fournisseurs de services procèdent à la période de temps qui s’écoule entre la première utilisation et la réutilisation dès que possible. En outre, l’identificateur d’entrée doit être réaffecté à un autre objet du même type. Autrement dit, un identificateur d’entrée particulier ne doit pas être associé à tout d’abord avec un message, puis avec un dossier.
  
## <a name="see-also"></a>Voir aussi



[Identificateurs d’entrée MAPI](mapi-entry-identifiers.md)

