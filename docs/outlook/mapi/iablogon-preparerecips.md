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
ms.openlocfilehash: 0a9b88d762ca88cebd6d9acecf06db53a0b778f6
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33423859"
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

## <a name="parameters"></a>Paramètres

_ulFlags_
  
> dans Masque de des indicateurs qui contrôle le type du texte dans les chaînes renvoyées. L'indicateur suivant peut être défini:
    
  - MAPI_CACHE_ONLY: Utilisez uniquement le carnet d'adresses en mode hors connexion pour effectuer la résolution de noms. Par exemple, vous pouvez utiliser cet indicateur pour permettre à une application cliente d'ouvrir la liste d'adresses globale (LAG) en mode Exchange mis en cache et d'accéder à une entrée de ce carnet d'adresses à partir du cache sans créer de trafic entre le client et le serveur. Cet indicateur est pris en charge uniquement par le fournisseur de carnet d'adresses Exchange.
    
_lpPropTagArray_
  
> dans Pointeur vers une structure [SPropTagArray](sproptagarray.md) qui contient un tableau de balises de propriété indiquant les propriétés qui nécessitent une mise à jour, le cas échéant. Le paramètre _lpPropTagArray_ peut être null. 
    
_lpRecipList_
  
> dans Pointeur vers une structure [ADRLIST](adrlist.md) qui contient la liste des destinataires. 
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> La liste des destinataires a été préparée.
    
MAPI_E_NOT_FOUND 
  
> Au moins un des destinataires dans le paramètre _lpRecipList_ n'existe pas. 
    
## <a name="return-value"></a>Valeur renvoyée

Un client appelle la méthode MAPI [IAddrBook::P reparerecips](iaddrbook-preparerecips.md) pour modifier ou réorganiser un ensemble de propriétés pour un ou plusieurs destinataires. Les destinataires peuvent ou non faire partie de la liste des destinataires d'un message sortant. MAPI transfère cet appel à la méthode IABLogon du fournisseur de carnet d'adresses **::P reparerecips** . 
  
**IABLogon::P reparerecips** effectue quatre tâches principales: 
  
- Garantit que tous les destinataires de la liste d'adresses vers laquelle pointe le paramètre _lpRecipList_ ont un identificateur d'entrée à long terme. 
    
- Garantit que tous les destinataires ont les propriétés spécifiées dans le tableau de valeurs de propriété vers lequel pointe le paramètre _lpPropTagArray_ . 
    
- Garantit que les propriétés du tableau de valeurs de propriété apparaissent avant les autres propriétés qui existaient avant l'appel.
    
- Garantit que l'ordre des propriétés dans la structure [ADRENTRY](adrentry.md) de chaque destinataire dans la structure **ADRLIST** est le même que dans le tableau de valeurs de la propriété. 
    
La structure **ADRENTRY** dans le paramètre _lpRecipList_ contient une structure **ADRENTRY** pour chaque destinataire. Chaque structure **ADRENTRY** contient un tableau de structures [SPropValue](spropvalue.md) pour décrire les propriétés du destinataire. Lorsque **IABLogon::P reparerecips** renvoie, le tableau de structures **SPropValue** pour chaque destinataire inclut les propriétés de l' _lpPropTagArray_ suivies par les autres propriétés du destinataire. 
  
## <a name="notes-to-implementers"></a>Remarques pour les responsables de l’implémentation

Implémentation de **IABLogon::P reparerecips** implique de placer des propriétés dans un ordre spécifique, d'extraire des valeurs de propriétés et de convertir des identificateurs d'entrée à court terme en identificateurs d'entrée à long terme. Les propriétés qui sont demandées dans le paramètre _lpPropTagArray_ doivent se trouver au début du tableau de valeurs de la propriété associé à la structure **ADRENTRY** de chaque destinataire dans le paramètre _lpRecipList_ . Si les valeurs de ces propriétés n'existent pas, ouvrez l'utilisateur de messagerie associé ou la liste de distribution à l'aide de son identificateur d'entrée et récupérez les valeurs de propriété manquantes. 
  
AlLouez chaque structure **SPropValue** passée dans _lpRecipList_ séparément afin que les structures puissent être libérées individuellement. Si vous devez allouer de l'espace supplémentaire pour une structure **SPropValue** , par exemple, pour stocker les données d'une propriété de type chaîne, utilisez la fonction [MAPIAllocateBuffer](mapiallocatebuffer.md) pour allouer de l'espace supplémentaire pour le tableau de valeurs de la propriété complète. Utilisez la fonction [MAPIFreeBuffer](mapifreebuffer.md) pour libérer le tableau de valeurs de propriété d'origine, puis utilisez la fonction [MAPIAllocateMore](mapiallocatemore.md) pour allouer toute mémoire supplémentaire requise. 
  
Pour implémenter **IABLogon::P reparerecips**, procédez comme suit:
  
1. Vérifiez les entrées dans le paramètre _lpPropTagArray_ . Si le tableau de valeurs de la propriété est vide, il n'y a aucun travail à faire. Renvoyer une valeur de réussite. 
    
2. Traitez chaque destinataire dans le paramètre _lpRecipList_ . Il existe un membre de structure **ADRENTRY** pour chaque destinataire dans la liste. Ignorez les types de destinataires suivants: 
    
   - Destinataires sans identificateur d'entrée dans le membre **rgPropVals** de leur structure **ADRENTRY** (c'est-à-dire, destinataires non résolus). 
    
   - Les destinataires dont l'identificateur d'entrée n'appartient pas à votre fournisseur. Ces destinataires seront transmis à un autre fournisseur de carnets d'adresses.
    
3. Ouvrez le destinataire et extrayez les propriétés qui sont déjà définies pour le destinataire.
    
4. Fusionnez le tableau de valeurs de propriété spécifié dans _lpRecipList_ avec le tableau de propriétés renvoyées à partir de **GetProps**. Si la même propriété se produit dans les deux tableaux de propriétés, utilisez la valeur de _lpRecipList_.
    
5. Si le tableau de valeurs de la propriété _lpRecipList_ est suffisamment grand pour contenir toutes les propriétés nécessaires, il suffit de le remplacer par le tableau fusionné. Si le tableau de valeurs de la propriété _lpRecipList_ n'est pas assez grand, remplacez-le par un tableau nouvellement alloué. Assurez-vous que le nouveau tableau dispose d'une valeur mise à jour dans chacun de ses membres **cValues** . 
    
6. Si vous ne connaissez pas une ou plusieurs des propriétés du paramètre _lpPropTagArray_ , définissez le type de la propriété dans la structure **ADRENTRY** du destinataire sur PT_ERROR et la valeur de la propriété sur MAPI_E_NOT_FOUND ou sur une autre valeur qui donne plus raison spécifique de l'indisponibilité de la propriété. Pour plus d'informations sur PT_ERROR, consultez la rubrique [types de propriétés](property-types.md).
    
> [!NOTE]
> Ne réaffectez jamais la structure **ADRLIST** passée dans **IABLogon::P reparerecips** ou modifier son nombre d'entrées. 
  
## <a name="see-also"></a>Voir aussi

- [ADRLIST](adrlist.md)
- [IMAPIProp::GetProps](imapiprop-getprops.md)
- [Propriété canonique PidTagEntryId](pidtagentryid-canonical-property.md)
- [SPropValue](spropvalue.md)
- [IABLogon : IUnknown](iablogoniunknown.md)

