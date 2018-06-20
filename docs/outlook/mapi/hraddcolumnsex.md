---
title: HrAddColumnsEx
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.HrAddColumnsEx
api_type:
- COM
ms.assetid: c0a65d2b-a9b8-4477-a1c7-18c8478126f6
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: c79d9ebb5be1d8af6c9136514d8a2b695513f755
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19783519"
---
# <a name="hraddcolumnsex"></a>HrAddColumnsEx

  
  
**S’applique à**: Outlook 
  
Ajoute ou déplacer des colonnes au début d’une table existante. 
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapiutil.h  <br/> |
|Implémentée par :  <br/> |MAPI  <br/> |
|Appelée par :  <br/> |Les applications clientes et des fournisseurs de services  <br/> |
   
```cpp
HRESULT HrAddColumnsEx(
  LPMAPITABLE lptbl,
  LPSPropTagArray lpproptagColumnsNew,
  LPALLOCATEBUFFER lpAllocateBuffer,
  LPFREEBUFFER lpFreeBuffer,
  void (FAR * lpfnFilterColumns)(
  LPSPropTagArray ptaga)
);
```

## <a name="parameters"></a>Paramètres

 _lptbl_
  
> [in] Pointeur vers le tableau MAPI affecté. 
    
 _lpproptagColumnsNew_
  
> [in] Pointeur vers une structure [SPropTagArray](sproptagarray.md) qui contient un tableau de balises de propriété pour les propriétés à ajouter ou déplacées vers le début de la table. 
    
 _lpAllocateBuffer_
  
> [in] Pointeur vers la fonction [MAPIAllocateBuffer](mapiallocatebuffer.md) , à utiliser pour allouer de la mémoire. 
    
 _lpFreeBuffer_
  
> [in] Pointeur vers la fonction [MAPIFreeBuffer](mapifreebuffer.md) , à utiliser pour libérer de la mémoire. 
    
 _lpfnFilterColumns_
  
> [in] Pointeur vers une fonction de rappel fournie par l’appelant. Si le paramètre _lpfnFilterColumns_ est défini sur NULL, aucun rappel n’est effectuée. 
    
 _ptaga_
  
> [in] Pointeur vers une structure [SPropTagArray](sproptagarray.md) qui contient le tableau des balises de propriété existant déjà dans la table avant de propriétés sont ajoutées ou déplacées vers le début. Passe **HrAddColumnsEx** ce pointeur en tant que paramètre à la fonction de rappel désigné par _lpfnFilterColumns_.
    
## <a name="return-value"></a>Valeur renvoy�e

S_OK 
  
> L’appel a réussi et les colonnes spécifiées ont été déplacés ou ajoutés.
    
## <a name="remarks"></a>Remarques

Les propriétés transmises à **HrAddColumnsEx** en utilisant le paramètre _lpproptagColumnsNew_ deviennent les propriétés de premières exposées sur les appels suivants à la méthode [IMAPITable::QueryRows](imapitable-queryrows.md) . Toutes les propriétés précédemment dans le tableau qui n’est pas spécifiées dans le paramètre _lpproptagColumnsNew_ sont exposées après toutes les propriétés ajoutées et déplacées. 
  
Si les propriétés du tableau ne sont pas définies lorsque **QueryRows** est appelée, ils sont retournées avec le type de la propriété PT_NULL et l’identificateur de la propriété PROP_ID_NULL. 
  
## <a name="notes-to-callers"></a>Notes aux appelants

La fonction **HrAddColumnsEx** permet à l’appelant de fournir une fonction de rappel pour filtrer les colonnes qui étaient déjà dans le tableau, par exemple pour convertir des chaînes en type de propriété PT_UNICODE PT_STRING8. **HrAddColumnsEx** passe un pointeur vers la colonne existaient précédemment défini en tant que paramètre à la fonction de rappel. La fonction de rappel peut modifier des données dans le tableau de la propriété tag, mais ne peut pas ajouter de nouvelles balises. 
  
 **HrAddColumnsEx** appelle d’abord la fonction de rappel s’il est fourni, puis ajoute ou déplace les colonnes spécifiées et enfin appelle [IMAPITable::SetColumns](imapitable-setcolumns.md). 
  
Les paramètres d’entrée _lpAllocateBuffer_ et _lpFreeBuffer_ pointent vers les fonctions [MAPIAllocateBuffer](mapiallocatebuffer.md) et [MAPIFreeBuffer](mapifreebuffer.md) , respectivement. Les valeurs exactes des pointeurs transmis à **HrAddColumnsEx** dépendent si l’appelant est une application cliente ou un fournisseur de services. Un client transmet des pointeurs vers les fonctions MAPI portant le nom spécifié. Un fournisseur de services transmet les pointeurs qu’elle reçue dans son appel d’initialisation ou récupéré en appelant la méthode [IMAPISupport::GetMemAllocRoutines](imapisupport-getmemallocroutines.md) . 
  
## <a name="see-also"></a>Voir aussi



[IMAPITable::QueryColumns](imapitable-querycolumns.md)

