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
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: c77acb5226361ce31a7f6b1694de7fe23f8dd71b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33415270"
---
# <a name="entryid"></a>ENTRYID

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient un identificateur d'entrée pour un objet MAPI. 
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapidefs. h  <br/> |
|Macros connexes:  <br/> |[CbNewENTRYID](cbnewentryid.md), [SizedENTRYID](sizedentryid.md) <br/> |
   
```cpp
typedef struct
{
  BYTE abFlags[4];
  BYTE ab[MAPI_DIM];
} ENTRYID, FAR *LPENTRYID;

```

## <a name="members"></a>Members

 **abFlags**
  
> Masque de des indicateurs qui fournissent des informations décrivant l'objet. Seul le premier octet des indicateurs, **abFlags [0]**, peut être défini par le fournisseur; les trois autres sont réservés. Ces indicateurs ne doivent pas être définis pour les identificateurs d'entrée permanents; elles sont définies uniquement pour les identificateurs d'entrée à court terme. Pour les clients, cette structure est en lecture seule. Les indicateurs suivants peuvent être définis dans **abFlags [0]**:
    
MAPI_NOTRECIP 
  
> L'identificateur d'entrée ne peut pas être utilisé comme destinataire sur un message.
    
MAPI_NOTRESERVED 
  
> Les autres utilisateurs ne peuvent pas accéder à l'identificateur d'entrée.
    
MAPI_NOW 
  
> L'identificateur d'entrée ne peut pas être utilisé à d'autres moments.
    
MAPI_SHORTTERM 
  
> L'identificateur d'entrée est à court terme. Toutes les autres valeurs de cet octet doivent être définies sauf si les autres utilisations de l'identificateur d'entrée sont activées.
    
MAPI_THISSESSION 
  
> L'identificateur d'entrée ne peut pas être utilisé pour d'autres sessions.
    
 **opér**
  
> Indique un tableau de données binaires utilisées par les fournisseurs de services. L'application cliente ne peut pas utiliser ce tableau.
    
## <a name="remarks"></a>Remarques

La structure **EntryID** est utilisée par les fournisseurs de banques de messages et de carnet d'adresses pour construire des identificateurs uniques pour leurs objets. Les identificateurs d'entrée sont utilisés pour identifier les types d'objets suivants: 
  
- Banques de messages
    
- Folders
    
- Messages
    
- Conteneurs du carnet d'adresses
    
- Listes de distribution
    
- Utilisateurs de messagerie
    
- Objets de statut
    
- Sections de profil
    
Chaque fournisseur utilise un format pour la structure **EntryID** qui est logique pour ce fournisseur. 
  
Chaque identificateur d'entrée ne peut être comparé directement, car un objet peut être représenté par deux valeurs binaires différentes. Pour déterminer si deux identificateurs d'entrée représentent le même objet, appelez la méthode [IMAPISession:: CompareEntryIDs](imapisession-compareentryids.md) . 
  
Lorsqu'un client appelle la méthode [IMAPIProp:: GetProps](imapiprop-getprops.md) d'un objet pour récupérer son identificateur d'entrée, l'objet renvoie la forme la plus permanente de l'identificateur d'entrée. Un client peut vérifier qu'un identificateur d'entrée est à long terme en vérifiant qu'aucun des indicateurs n'est défini dans le premier octet du membre **abFlags** . 
  
Lorsqu'un client accède à un identificateur d'entrée par le biais d'une colonne dans une table, il est probable que cet identificateur d'entrée soit à court terme au lieu de long terme. Les identificateurs d'entrée à court terme peuvent être utilisés pour ouvrir leurs objets correspondants uniquement dans la session MAPI actuelle. Un client peut vérifier qu'un identificateur d'entrée est à court terme en vérifiant que tous les indicateurs sont définis dans le premier octet du membre **abFlags** . 
  
Certains identificateurs d'entrée sont à court terme, mais ont une utilisation à long terme. Un ou plusieurs indicateurs appropriés doivent être définis dans le premier octet de son membre **abFlags** pour un identificateur d'entrée. 
  
Une structure **EntryID** ressemble à une structure [FLATENTRY](flatentry.md) . Toutefois, il existe quelques différences: 
  
- Une structure **EntryID** ne stocke pas la taille de l'identificateur d'entrée; une structure **FLATENTRY** . 
    
- Une structure **EntryID** stocke les données d'indicateur et le reste de l'identificateur d'entrée séparément; une structure **FLATENTRY** stocke les données d'indicateur avec le reste de l'identificateur d'entrée. 
    
- Une structure **EntryID** est transmise en tant que paramètre aux méthodes de l'interface [IMAPIProp](imapipropiunknown.md) et aux méthodes **OpenEntry** suivantes: [IABLogon:: OpenEntry](iablogon-openentry.md), [IAddrBook:: OpenEntry](iaddrbook-openentry.md), [IMAPIContainer:: OpenEntry ](imapicontainer-openentry.md), [IMAPISession:: OpenEntry](imapisession-openentry.md), [IMAPISupport:: OpenEntry](imapisupport-openentry.md), [IMsgStore:: OpenEntry](imsgstore-openentry.md), IMSLogon: [: OpenEntry](imslogon-openentry.md)
    
- Une structure **EntryID** est utilisée pour stocker un identificateur d'entrée sur le disque. Une structure **FLATENTRY** est utilisée pour stocker un identificateur d'entrée dans un fichier ou le transmettre dans un flux d'octets. 
    
Les clients doivent toujours transmettre des identificateurs d'entrée naturellement alignés. Bien que les fournisseurs doivent gérer des identificateurs d'entrée arbitrairement alignés, les clients ne doivent pas s'attendre à ce comportement. Le fait de ne pas transmettre un identificateur d'entrée correctement aligné à une méthode peut entraîner une erreur d'alignement sur les processeurs RISC. 
  
Le facteur d'alignement naturel, généralement 8 octets, est le plus grand type de données pris en charge par l'UC et généralement le même facteur d'alignement utilisé par l'allocateur de mémoire système. Une adresse de mémoire naturellement alignée permet au processeur d'accéder à n'importe quel type de données pris en charge à cette adresse sans générer de faute d'alignement. Pour les processeurs RISC, un type de données de taille N octets doit généralement être aligné sur un multiple pair de N octets, l'adresse étant un multiple pair de N.
  
Pour plus d'informations, consultez la rubrique identificateurs d' [entrée](mapi-entry-identifiers.md). 
  
## <a name="see-also"></a>Voir aussi



[FLATENTRY](flatentry.md)
  
[IMAPISupport::CompareEntryIDs](imapisupport-compareentryids.md)
  
[Propriété canonique PidTagRecordKey](pidtagrecordkey-canonical-property.md)


[Structures MAPI](mapi-structures.md)

