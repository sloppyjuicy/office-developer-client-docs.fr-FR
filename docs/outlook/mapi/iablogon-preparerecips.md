---
title: IABLogonPrepareRecips
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IABLogon.PrepareRecips
api_type:
- COM
ms.assetid: 3c1845ea-e291-4855-9afd-51d2c64d7e85
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: c42077528a4f7227321d8f987cc5dd0ccd4c966c
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22589741"
---
# <a name="iablogonpreparerecips"></a>IABLogon::PrepareRecips

**S’applique à** : Outlook 2013 | Outlook 2016 
  
Prépare une liste de destinataires pour une utilisation ultérieure par le système de messagerie.
  
```cpp
HRESULT PrepareRecips(
  ULONG ulFlags,
  LPSPropTagArray lpPropTagArray,
  LPADRLIST lpRecipList
);
```

## <a name="parameters"></a>Param�tres

_ulFlags_
  
> [in] Masque de bits d’indicateurs qui contrôle le type du texte dans les chaînes retournées. Vous pouvez définir l’indicateur suivant :
    
  - MAPI_CACHE_ONLY : Utilisez uniquement le carnet d’adresses en mode hors connexion pour effectuer la résolution de noms. Par exemple, vous pouvez utiliser cet indicateur pour autoriser une application cliente ouvrir la liste d’adresses globale (LAG) en mode exchange mis en cache et accéder à une entrée dans ce carnet d’adresses à partir du cache sans créer le trafic entre le client et le serveur. Cet indicateur est pris en charge uniquement par le fournisseur de carnet d’adresses Exchange.
    
_lpPropTagArray_
  
> [in] Pointeur vers une structure [SPropTagArray](sproptagarray.md) qui contient un tableau de balises de propriétés qui indiquent les propriétés qui nécessitent la mise à jour, le cas échéant. Le paramètre _lpPropTagArray_ peut être NULL. 
    
_lpRecipList_
  
> [in] Pointeur vers une structure [ADRLIST](adrlist.md) qui contenue la liste des destinataires. 
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> La liste de destinataires a été correctement préparée.
    
MAPI_E_NOT_FOUND 
  
> Une ou plusieurs des destinataires dans le paramètre _lpRecipList_ n’existent pas. 
    
## <a name="return-value"></a>Valeur renvoyée

Un client appelle la méthode MAPI [IAddrBook::PrepareRecips](iaddrbook-preparerecips.md) pour modifier ou réorganiser un ensemble de propriétés pour un ou plusieurs destinataires. Les destinataires peuvent ou ne peuvent pas faire partie de la liste des destinataires d’un message sortant. MAPI transfère cet appel à la méthode de **IABLogon::PrepareRecips** d’un fournisseur de carnet d’adresses. 
  
**IABLogon::PrepareRecips** effectue les quatre tâches principales : 
  
- Garantit que tous les destinataires dans la liste d’adresses vers lesquelles pointent par le paramètre _lpRecipList_ ont un identificateur d’entrée à long terme. 
    
- Garantit que tous les destinataires ont les propriétés spécifiées dans le tableau de valeurs de propriété indiqué par le paramètre _lpPropTagArray_ . 
    
- Garantit que les propriétés du tableau de valeur de propriété s’affichent avant les autres propriétés qui existaient avant l’appel.
    
- Garantit que l’ordre des propriétés de la structure [ADRENTRY](adrentry.md) de chaque destinataire de la structure **ADRLIST** est le même que dans le tableau de valeurs de propriété. 
    
La structure **ADRENTRY** dans le paramètre _lpRecipList_ contient une structure **ADRENTRY** pour chaque destinataire. Chaque structure **ADRENTRY** contient un tableau de structures [SPropValue](spropvalue.md) pour décrire les propriétés du destinataire. **IABLogon::PrepareRecips** retourne le tableau de structure **SPropValue** pour chaque destinataire inclut les propriétés de l' _lpPropTagArray_ suivi par les autres propriétés pour le destinataire. 
  
## <a name="notes-to-implementers"></a>Remarques à l’attention des responsables de l’implémentation

L’implémentation **IABLogon::PrepareRecips** implique l’assignation de propriétés dans un ordre spécifique, extraction de valeurs de propriété et la conversion des identificateurs d’entrée à court terme pour les identificateurs d’entrée à long terme. Les propriétés qui sont demandées dans le paramètre _lpPropTagArray_ doivent être au début du tableau de valeur de propriété associé à **ADRENTRY** structure chaque destinataire dans le paramètre _lpRecipList_ . Si les valeurs de ces propriétés n’existent pas, ouvrez la liste associée d’utilisateur ou de distribution de messagerie à l’aide de son identificateur d’entrée et récupérer les valeurs de propriété manquantes. 
  
Allouer chaque structure **SPropValue** passé _lpRecipList_ séparément afin que les structures peuvent être libérés individuellement. Si vous devez allouer l’espace supplémentaire pour les structures **SPropValue** , par exemple, utilisez la fonction [MAPIAllocateBuffer](mapiallocatebuffer.md) pour stocker les données d’une propriété de chaîne, à allouer de l’espace supplémentaire pour le tableau de valeurs de propriété complète. Utilisez la fonction [MAPIFreeBuffer](mapifreebuffer.md) pour libérer le tableau de valeurs de propriété d’origine, puis utilisez la fonction [MAPIAllocateMore](mapiallocatemore.md) pour allouer toute mémoire supplémentaire est requis. 
  
Pour mettre en œuvre **IABLogon::PrepareRecips**, utilisez la procédure suivante :
  
1. Vérifiez les entrées dans le paramètre _lpPropTagArray_ . Si le tableau de valeurs de propriété est vide, il n’existe aucune tâche à effectuer. Renvoie une valeur de réussite. 
    
2. Processus de chaque destinataire dans le paramètre _lpRecipList_ . Il est un membre de la structure **ADRENTRY** pour chaque destinataire dans la liste. Ignorer les types de destinataires suivants : 
    
   - Destinataires sans un identificateur d’entrée dans le membre **rgPropVals** de leur structure **ADRENTRY** (autrement dit, les destinataires). 
    
   - Destinataires avec un identificateur d’entrée qui n’appartient pas à votre fournisseur. Ces destinataires sont communiquées à un autre fournisseur de carnet d’adresses.
    
3. Ouvrez le destinataire et récupérer les propriétés qui sont déjà définies pour le destinataire.
    
4. Le tableau de valeurs de propriété spécifié dans la _lpRecipList_ avec le tableau de propriétés renvoyé par **GetProps**de fusion. Si la même propriété se produit dans les deux tableaux de propriétés, utilisez la valeur de _lpRecipList_.
    
5. Si le tableau de valeurs de propriété _lpRecipList_ est suffisante pour contenir toutes les propriétés nécessaires, juste Remplacez-la par le tableau fusionné. Si le tableau de valeurs de propriété _lpRecipList_ n’est pas suffisante, remplacez-la par un tableau nouvellement allouée. Assurez-vous que le nouveau tableau comporte une valeur de mise à jour dans chacun de ses membres **cValues** . 
    
6. Si vous ne connaissez pas une ou plusieurs des propriétés dans le paramètre _lpPropTagArray_ , définir le type de propriété de structure **ADRENTRY** du destinataire PT_ERROR et la valeur de propriété à MAPI_E_NOT_FOUND ou à une autre valeur qui fournit une plus raison spécifique de l’indisponibilité de la propriété. Pour plus d’informations sur PT_ERROR, reportez-vous à [Types de propriété](property-types.md).
    
> [!NOTE]
> Ne jamais réaffecter la structure **ADRLIST** qui est passée dans **IABLogon::PrepareRecips** ou modifier son nombre d’entrées. 
  
## <a name="see-also"></a>Voir aussi

- [ADRLIST](adrlist.md)
- [IMAPIProp::GetProps](imapiprop-getprops.md)
- [Propriété canonique PidTagEntryId](pidtagentryid-canonical-property.md)
- [SPropValue](spropvalue.md)
- [IABLogon : IUnknown](iablogoniunknown.md)

