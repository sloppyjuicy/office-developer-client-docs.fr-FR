---
title: ADRLIST
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ADRLIST
api_type:
- COM
ms.assetid: 85f0d8a5-6dd3-4f33-b31a-246d286d6286
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 319c932862615e063a02ffac07e5541b1b20ac7e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32330242"
---
# <a name="adrlist"></a>ADRLIST

**S’applique à** : Outlook 2013 | Outlook 2016 
  
Décrit zéro ou plusieurs propriétés qui appartiennent à un ou plusieurs destinataires. 
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapidefs. h  <br/> |
|Macros connexes:  <br/> |[CbADRLIST](cbadrlist.md), [CbNewADRLIST](cbnewadrlist.md), [CbNewADRLIST](cbnewadrlist.md) <br/> |
   
```cpp
typedef struct _ADRLIST
{
  ULONG cEntries;
  ADRENTRY aEntries[MAPI_DIM];
} ADRLIST, FAR *LPADRLIST;

```

## <a name="members"></a>Membres

**cEntries**
  
> Nombre d'entrées dans le tableau spécifié par le membre **aEntries** . 
    
**aEntries**
  
> Tableau de structures [ADRENTRY](adrentry.md) , une structure pour chaque destinataire. 
    
## <a name="remarks"></a>Remarques

Une structure **ADRLIST** contient une ou plusieurs structures **ADRENTRY** , chacune décrivant les propriétés d'un destinataire. Un destinataire peut être non résolu. Cela signifie qu'il manque un identificateur d'entrée dans le tableau des valeurs de propriété. Un destinataire résolu signifie que la **propriété\_PR EntryID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) est incluse. En règle générale, les destinataires résolus ont également une adresse de messagerie de la propriété **PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md)). Toutefois, l'adresse de messagerie n'est pas obligatoire. Les structures **ADRLIST** sont utilisées, par exemple, pour décrire la liste des destinataires d'un message sortant et MAPI pour afficher les entrées du carnet d'adresses. 
  
Les structures **ADRLIST** ressemblent aux structures [SRowSet](srowset.md) les structures utilisées pour représenter les lignes dans les tableaux. En fait, ces deux structures sont conçues de manière à ce qu'elles puissent être utilisées indifféremment. Elles contiennent toutes deux un tableau de structures décrivant un groupe de propriétés et un nombre de valeurs dans le tableau. Contrairement à la structure **ADRLIST** , le tableau contient des structures [ADRENTRY](adrentry.md) , dans la structure **SRowSet** , le tableau contient des structures [SRow](srow.md) . Les structures **ADRENTRY** et **SRow** sont identiques dans la mise en page. Étant donné que les structures **ADRLIST** et **SRowSet** suivent les mêmes règles d'allocation, une structure **SRowSet** extraite de la table de contenu d'un conteneur de carnet d'adresses peut être convertie en une structure **ADRLIST** et utilisée comme c'est le cas. 
  
L'illustration suivante montre la disposition d'une structure **ADRLIST** . 
  
**Composants ADRLIST**
  
![Composants ADRLIST] (media/amapi_18.gif "Composants ADRLIST")
  
Les parties **ADRENTRY** et [SPropValue](spropvalue.md) dans une structure **ADRLIST** doivent être allouées et libérées indépendamment des autres parties. Autrement dit, chaque structure **SPropValue** doit être allouée individuellement après que la mémoire de la structure **ADRENTRY** a été allouée et libérée avant la libération de la structure **ADRENTRY** . Cette indépendance dans la gestion de la mémoire permet aux destinataires et aux propriétés des destinataires d'être librement ajoutés ou supprimés de la liste d'adresses. 
  
Les fonctions [MAPIAllocateBuffer](mapiallocatebuffer.md) et [MAPIFreeBuffer](mapifreebuffer.md) doivent être utilisées pour allouer et libérer la structure **ADRLIST** et tous ses composants. 
  
Si une liste de destinataires est trop volumineuse pour tenir dans la mémoire, les clients peuvent appeler la méthode [IMessage:: ModifyRecipients](imessage-modifyrecipients.md) pour fonctionner avec un sous-ensemble de la liste. Dans ce cas, les clients ne doivent pas utiliser les boîtes de dialogue communes du carnet d'adresses. 
  
Pour plus d'informations sur la façon d'allouer de la mémoire aux structures **ADRENTRY** , consultez la rubrique [Managing Memory for ADRLIST and SRowSet structures](managing-memory-for-adrlist-and-srowset-structures.md). 
  
## <a name="see-also"></a>Voir aussi

- [ADRENTRY](adrentry.md)  
- [CbNewADRLIST](cbnewadrlist.md) 
- [IMessage::ModifyRecipients](imessage-modifyrecipients.md) 
- [SRowSet](srowset.md)
- [Structures MAPI](mapi-structures.md)

