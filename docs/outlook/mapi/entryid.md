---
title: ENTRYID
description: ENTRYID contient un identificateur d’entrée pour un objet MAPI. Cet article décrit sa syntaxe, ses membres et ses remarques.
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.ENTRYID
api_type:
- COM
ms.assetid: 8ebb21ca-5ad1-4dcc-97b6-2390664b5d8d
ms.openlocfilehash: f352c4fd9b85488a9ad95a55e5ae1dce06d7031d
ms.sourcegitcommit: f872848fbeb5b2353179ad4bf4eab23f61f87666
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/01/2022
ms.locfileid: "65815855"
---
# <a name="entryid"></a>ENTRYID

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient un identificateur d’entrée pour un objet MAPI. 
  
|Propriété |Valeur |
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapidefs.h  <br/> |
|Macros associées :  <br/> |[CbNewENTRYID](cbnewentryid.md), [SizedENTRYID](sizedentryid.md) <br/> |
   
```cpp
typedef struct
{
  BYTE abFlags[4];
  BYTE ab[MAPI_DIM];
} ENTRYID, FAR *LPENTRYID;

```

## <a name="members"></a>Members

 **abFlags**
  
> Masque de bits des indicateurs qui fournissent des informations qui décrivent l’objet. Seul le premier octet des indicateurs, **abFlags[0]**, peut être défini par le fournisseur ; les trois autres sont réservés. Ces indicateurs ne doivent pas être définis pour les identificateurs d’entrée permanents ; ils sont uniquement définis pour les identificateurs d’entrée à court terme. Pour les clients, cette structure est en lecture seule. Les indicateurs suivants peuvent être définis dans **abFlags[0]** :
    
MAPI_NOTRECIP 
  
> L’identificateur d’entrée ne peut pas être utilisé comme destinataire sur un message.
    
MAPI_NOTRESERVED 
  
> Les autres utilisateurs ne peuvent pas accéder à l’identificateur d’entrée.
    
MAPI_NOW 
  
> L’identificateur d’entrée ne peut pas être utilisé à d’autres moments.
    
MAPI_SHORTTERM 
  
> L’identificateur d’entrée est à court terme. Toutes les autres valeurs de cet octet doivent être définies, sauf si d’autres utilisations de l’identificateur d’entrée sont activées.
    
MAPI_THISSESSION 
  
> L’identificateur d’entrée ne peut pas être utilisé sur d’autres sessions.
    
 **Ab**
  
> Indique un tableau de données binaires utilisées par les fournisseurs de services. L’application cliente ne peut pas utiliser ce tableau.
    
## <a name="remarks"></a>Remarques

La structure **ENTRYID** est utilisée par le magasin de messages et les fournisseurs de carnets d’adresses pour construire des identificateurs uniques pour leurs objets. Les identificateurs d’entrée sont utilisés pour identifier les types d’objets suivants : 
  
- Magasins de messages
    
- Folders
    
- Messages
    
- Conteneurs de carnets d’adresses
    
- Listes de distribution
    
- Utilisateurs de messagerie
    
- Objets de statut
    
- Sections de profil
    
Chaque fournisseur utilise un format pour la structure **ENTRYID** qui est logique pour ce fournisseur. 
  
Chaque identificateur d'entrée ne peut être comparé directement, car un objet peut être représenté par deux valeurs binaires différentes. Pour déterminer si deux identificateurs d’entrée représentent le même objet, appelez la méthode [IMAPISession::CompareEntryIDs](imapisession-compareentryids.md) . 
  
Lorsqu’un client appelle la méthode [IMAPIProp::GetProps](imapiprop-getprops.md) d’un objet pour récupérer son identificateur d’entrée, l’objet retourne la forme la plus permanente de l’identificateur d’entrée. Un client peut vérifier qu’un identificateur d’entrée est à long terme en vérifiant qu’aucun des indicateurs n’est défini dans le premier octet du membre **abFlags** . 
  
Lorsqu’un client accède à un identificateur d’entrée via une colonne d’une table, cet identificateur d’entrée est probablement à court terme plutôt qu’à long terme. Les identificateurs d’entrée à court terme peuvent être utilisés pour ouvrir leurs objets correspondants uniquement dans la session MAPI actuelle. Un client peut vérifier qu’un identificateur d’entrée est à court terme en vérifiant que tous les indicateurs sont définis dans le premier octet du membre **abFlags** . 
  
Certains identificateurs d’entrée sont à court terme, mais ont une utilisation à long terme. Un ou plusieurs indicateurs appropriés seront définis dans le premier octet de son membre **abFlags** . 
  
Une structure **ENTRYID** ressemble à une structure [FLATENTRY](flatentry.md) . Toutefois, il existe quelques différences : 
  
- Une structure **ENTRYID** ne stocke pas la taille de l’identificateur d’entrée ; une structure **FLATENTRY** le fait. 
    
- Une structure **ENTRYID** stocke les données d’indicateur et le reste de l’identificateur d’entrée séparément ; une structure **FLATENTRY** stocke les données d’indicateur avec le reste de l’identificateur d’entrée. 
    
- Une structure **ENTRYID** est passée en tant que paramètre aux méthodes de l’interface [IMAPIProp](imapipropiunknown.md) et aux méthodes **OpenEntry** suivantes : [IABLogon::OpenEntry](iablogon-openentry.md), [IAddrBook::OpenEntry](iaddrbook-openentry.md), [IMAPIContainer::OpenEntry](imapicontainer-openentry.md), [IMAPISession::OpenEntry](imapisession-openentry.md), [IMAPISupport::OpenEntry](imapisupport-openentry.md), [IMsgStore::OpenEntry](imsgstore-openentry.md), [IMSLogon::OpenEntry](imslogon-openentry.md)
    
- Une structure **ENTRYID** est utilisée pour stocker un identificateur d’entrée sur le disque. Une structure **FLATENTRY** est utilisée pour stocker un identificateur d’entrée dans un fichier ou le transmettre dans un flux d’octets. 
    
Les clients doivent toujours transmettre des identificateurs d’entrée alignés naturellement. Bien que les fournisseurs doivent gérer des identificateurs d’entrée alignés arbitrairement, les clients ne doivent pas s’attendre à ce comportement. Le fait de ne pas transmettre un bon identificateur d’entrée aligné à une méthode peut provoquer une erreur d’alignement sur les processeurs RISC. 
  
Le facteur d’alignement naturel, généralement 8 octets, est le plus grand type de données pris en charge par l’UC, et généralement le même facteur d’alignement que celui utilisé par l’allocateur de mémoire système. Une adresse mémoire alignée naturellement permet au processeur d’accéder à n’importe quel type de données qu’il prend en charge à cette adresse sans générer d’erreur d’alignement. Pour les processeurs RISC, un type de données de taille N octets doit généralement être aligné sur un même multiple d’octets N, l’adresse étant un même multiple de N.
  
Pour plus d’informations, consultez [Identificateurs d’entrée](mapi-entry-identifiers.md). 
  
## <a name="see-also"></a>Voir aussi



[FLATENTRY](flatentry.md)
  
[IMAPISupport::CompareEntryIDs](imapisupport-compareentryids.md)
  
[Propriété canonique PidTagRecordKey](pidtagrecordkey-canonical-property.md)


[Structures MAPI](mapi-structures.md)

