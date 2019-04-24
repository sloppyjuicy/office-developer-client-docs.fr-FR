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
ms.openlocfilehash: 9ca34fb2cce6e86c42e8e9525cd213f1008997d6
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32348369"
---
# <a name="hraddcolumnsex"></a>HrAddColumnsEx

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Ajoute ou déplace des colonnes au début d'une table existante. 
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapiutil. h  <br/> |
|Implémenté par :  <br/> |MAPI  <br/> |
|Appelé par :  <br/> |Applications clientes et fournisseurs de services  <br/> |
   
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
  
> dans Pointeur vers le tableau MAPI affecté. 
    
 _lpproptagColumnsNew_
  
> dans Pointeur vers une structure [SPropTagArray](sproptagarray.md) qui contient un tableau de balises de propriété pour les propriétés à ajouter ou déplacer au début du tableau. 
    
 _lpAllocateBuffer_
  
> dans Pointeur vers la fonction [MAPIAllocateBuffer](mapiallocatebuffer.md) à utiliser pour allouer de la mémoire. 
    
 _lpFreeBuffer_
  
> dans Pointeur vers la fonction [MAPIFreeBuffer](mapifreebuffer.md) à utiliser pour libérer de la mémoire. 
    
 _lpfnFilterColumns_
  
> dans Pointeur vers une fonction de rappel fournie par l'appelant. Si le paramètre _lpfnFilterColumns_ est défini sur null, aucun rappel n'est effectué. 
    
 _ptaga_
  
> dans Pointeur vers une structure [SPropTagArray](sproptagarray.md) qui contient le tableau de balises de propriété déjà présentes dans le tableau avant l'ajout ou le déplacement des propriétés vers le début. **HrAddColumnsEx** transmet ce pointeur en tant que paramètre à la fonction de rappel pointée par _lpfnFilterColumns_.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> L'appel a réussi et les colonnes spécifiées ont été déplacées ou ajoutées.
    
## <a name="remarks"></a>Remarques

Les propriétés transmises à **HrAddColumnsEx** à l'aide du paramètre _lpproptagColumnsNew_ deviennent les premières propriétés exposées lors des appels suivants de la méthode [IMAPITable:: QueryRows](imapitable-queryrows.md) . Les propriétés précédemment répertoriées dans le tableau qui n'ont pas été spécifiées dans le paramètre _lpproptagColumnsNew_ sont exposées après toutes les propriétés ajoutées et déplacées. 
  
Si les propriétés d'une table ne sont pas définies lors de l'appel de **QueryRows** , elles sont renvoyées avec le type de propriété PT_NULL et l'identificateur de propriété PROP_ID_NULL. 
  
## <a name="notes-to-callers"></a>Remarques pour les appelants

La fonction **HrAddColumnsEx** permet à l'appelant de fournir une fonction de rappel pour filtrer les colonnes qui se trouvaient déjà dans la table, par exemple pour convertir les chaînes de type PT_UNICODE en PT_STRING8. **HrAddColumnsEx** transmet un pointeur vers le jeu de colonnes précédemment existant en tant que paramètre de la fonction de rappel. La fonction de rappel peut modifier des données dans le tableau de balises de propriété, mais ne peut pas ajouter de nouvelles balises. 
  
 **HrAddColumnsEx** appelle d'abord la fonction de rappel si elle est fournie, puis ajoute ou déplace les colonnes spécifiées, et enfin, il appelle la méthode [IMAPITable:: SetColumns](imapitable-setcolumns.md). 
  
Les paramètres d'entrée _lpAllocateBuffer_ et _lpFreeBuffer_ pointent vers les fonctions [MAPIAllocateBuffer](mapiallocatebuffer.md) et [MAPIFreeBuffer](mapifreebuffer.md) , respectivement. Les valeurs exactes des pointeurs transmis à **HrAddColumnsEx** varient selon que l'appelant est une application cliente ou un fournisseur de services. Un client passe des pointeurs aux fonctions MAPI avec les noms spécifiés. Un fournisseur de services transmet les pointeurs reçus dans son appel d'initialisation ou les récupère en appelant la méthode [IMAPISupport:: GetMemAllocRoutines](imapisupport-getmemallocroutines.md) . 
  
## <a name="see-also"></a>Voir aussi



[IMAPITable::QueryColumns](imapitable-querycolumns.md)

