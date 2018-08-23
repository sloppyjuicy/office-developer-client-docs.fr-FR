---
title: ENTRYID
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.ENTRYID
api_type:
- COM
ms.assetid: 8ebb21ca-5ad1-4dcc-97b6-2390664b5d8d
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: 8540176b7675917dde7c618c40142605e9622282
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22586220"
---
# <a name="entryid"></a>ENTRYID

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
Contient un identificateur d’entrée pour un objet MAPI. 
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapidefs.h  <br/> |
|Macros connexes :  <br/> |[CbNewENTRYID](cbnewentryid.md), [SizedENTRYID](sizedentryid.md) <br/> |
   
```cpp
typedef struct
{
  BYTE abFlags[4];
  BYTE ab[MAPI_DIM];
} ENTRYID, FAR *LPENTRYID;

```

## <a name="members"></a>Members

 **abFlags**
  
> Masque de bits des indicateurs qui fournissent des informations décrivant l’objet. Seul le premier octet des indicateurs, **abFlags [0]**, peut-être être défini par le fournisseur ; les trois autres sont réservés. Ces indicateurs ne doivent pas être définis pour les identificateurs d’entrée définitive ; ils sont définis uniquement pour les identificateurs d’entrée à court terme. Pour les clients, cette structure est en lecture seule. Les indicateurs suivants peuvent être définis dans **abFlags [0]**:
    
MAPI_NOTRECIP 
  
> L’identificateur d’entrée ne peut pas être utilisé en tant que destinataire d’un message.
    
MAPI_NOTRESERVED 
  
> Les autres utilisateurs ne peuvent pas accéder à l’identificateur d’entrée.
    
MAPI_NOW 
  
> L’identificateur d’entrée ne peut pas être utilisé à d’autres moments.
    
MAPI_SHORTTERM 
  
> L’identificateur d’entrée est à court terme. Toutes les autres valeurs dans cet octet doivent être définies à moins que les autres utilisations de l’identificateur d’entrée sont activées.
    
MAPI_THISSESSION 
  
> L’identificateur d’entrée ne peut pas être utilisé sur d’autres sessions.
    
 **Carnet d’adresses**
  
> Indique un tableau de données binaires qui sont utilisées par les fournisseurs de services. L’application cliente ne peut pas utiliser ce tableau.
    
## <a name="remarks"></a>Remarques

La structure de la **propriété ENTRYID** est utilisée par message stocker et pour construire des identificateurs uniques pour leurs objets des fournisseurs de carnet de d'adresses. Identificateurs d’entrée sont utilisés pour identifier les types d’objets suivants : 
  
- Banques de messages
    
- Dossiers
    
- Messages
    
- Conteneurs de carnet d’adresses
    
- Listes de distribution
    
- Les utilisateurs de messagerie
    
- Objets d’état
    
- Sections de profil
    
Chaque fournisseur utilise un format de la structure **ENTRYID** significatif pour ce fournisseur. 
  
Identificateurs d’entrée ne peut pas être comparées directement, car un objet peut être représenté par deux valeurs binaires différentes. Pour déterminer si deux identificateurs d’entrée représentent le même objet, appelez la méthode [IMAPISession::CompareEntryIDs](imapisession-compareentryids.md) . 
  
Lorsqu’un client appelle la méthode [IMAPIProp::GetProps](imapiprop-getprops.md) d’un objet à récupérer son identificateur d’entrée, l’objet retourne la forme plus définitive de l’identificateur d’entrée. Un client peut vérifier qu’un identificateur d’entrée est à long terme en vérifiant qu’aucun des indicateurs sont définis dans le premier octet du membre **abFlags** . 
  
Lorsqu’un client accède à un identificateur d’entrée à une colonne dans une table, probablement que cet identificateur d’entrée est à court terme au lieu à long terme. Identificateurs d’entrée à court terme peuvent servir à ouvrir les objets correspondants uniquement dans la session MAPI en cours. Un client peut vérifier qu’un identificateur d’entrée est à court terme en vérifiant que tous les indicateurs sont définis dans le premier octet du membre **abFlags** . 
  
Identificateurs d’entrée sont à court terme, mais utilisez à long terme. Identificateur entrée aura une ou plusieurs des indicateurs appropriés définis dans le premier octet de ses membres **abFlags** . 
  
Une structure **ENTRYID** ressemble à une structure [FLATENTRY](flatentry.md) . Toutefois, il existe quelques différences : 
  
- Une structure **ENTRYID** n’incluent pas la taille de l’identificateur d’entrée. une structure **FLATENTRY** fait. 
    
- Une structure **ENTRYID** stocke les données d’indicateur et le reste de l’identificateur d’entrée séparément ; une structure **FLATENTRY** stocke les données d’indicateur avec le reste de l’identificateur d’entrée. 
    
- Une structure **ENTRYID** est transmise en tant que paramètre aux méthodes de l’interface [IMAPIProp](imapipropiunknown.md) et aux méthodes **OpenEntry** suivantes : [IABLogon::OpenEntry](iablogon-openentry.md), [IAddrBook::OpenEntry](iaddrbook-openentry.md), [IMAPIContainer::OpenEntry ](imapicontainer-openentry.md), [IMAPISession::OpenEntry](imapisession-openentry.md), [IMAPISupport::OpenEntry](imapisupport-openentry.md), [IMsgStore::OpenEntry](imsgstore-openentry.md), [IMSLogon::OpenEntry](imslogon-openentry.md)
    
- Une structure **ENTRYID** est utilisée pour stocker un identificateur d’entrée sur le disque. Une structure **FLATENTRY** sert à stocker un identificateur d’entrée dans un fichier ou passez-la dans un flux d’octets. 
    
Clients doivent toujours passer dans les identificateurs d’entrée aligné naturellement. Bien que les fournisseurs doivent gérer les identificateurs d’entrée arbitrairement aligné, clients pas ce comportement sont normal. Passer un identificateur d’entrée aligné bonne à une méthode peut provoquer une erreur d’alignement sur les processeurs RISC. 
  
Le facteur d’alignement naturel, généralement 8 octets, est le plus grand type de données pris en charge par l’UC et généralement le même facteur d’alignement utilisé par l’allocation de mémoire système. Une adresse de la mémoire alignée naturellement permet de l’UC accéder à n’importe quel type de données que pris en charge à l’adresse sans générer une erreur d’alignement. Pour les processeurs RISC, un type de données de taille N doit généralement être aligné sur un multiple de N octets, avec l’adresse est un multiple de N.
  
Pour plus d’informations, voir [Identificateurs d’entrée](mapi-entry-identifiers.md). 
  
## <a name="see-also"></a>Voir aussi



[FLATENTRY](flatentry.md)
  
[IMAPISupport::CompareEntryIDs](imapisupport-compareentryids.md)
  
[Propriété canonique PidTagRecordKey](pidtagrecordkey-canonical-property.md)


[Structures MAPI](mapi-structures.md)

