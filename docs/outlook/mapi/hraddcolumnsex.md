---
title: HrAddColumnsEx
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.HrAddColumnsEx
api_type:
- COM
ms.assetid: c0a65d2b-a9b8-4477-a1c7-18c8478126f6
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 37651071bdc3ae99b4f374dcb7864a8f31dc1246
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59614065"
---
# <a name="hraddcolumnsex"></a>HrAddColumnsEx

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Ajoute ou déplace des colonnes au début d’un tableau existant. 
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapiutil.h  <br/> |
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
  
> [in] Pointeur vers la table MAPI affectée. 
    
 _lpproptagColumnsNew_
  
> [in] Pointeur vers une structure [SPropTagArray](sproptagarray.md) qui contient un tableau de balises de propriétés pour les propriétés à ajouter ou déplacer au début du tableau. 
    
 _lpAllocateBuffer_
  
> [in] Pointeur vers la [fonction MAPIAllocateBuffer,](mapiallocatebuffer.md) à utiliser pour allouer de la mémoire. 
    
 _lpFreeBuffer_
  
> [in] Pointeur vers la [fonction MAPIFreeBuffer,](mapifreebuffer.md) à utiliser pour libérer de la mémoire. 
    
 _lpfnFilterColumns_
  
> [in] Pointeur vers une fonction de rappel fournie par l’appelant. Si le  _paramètre lpfnFilterColumns est_ définie sur NULL, aucun rappel n’est effectué. 
    
 _ptaga_
  
> [in] Pointeur vers une structure [SPropTagArray](sproptagarray.md) qui contient le tableau des balises de propriétés qui existent déjà dans le tableau avant que les propriétés ne soient ajoutées ou déplacées au début. **HrAddColumnsEx** passe ce pointeur comme paramètre à la fonction de rappel pointée par  _lpfnFilterColumns_.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> L’appel a réussi et les colonnes spécifiées ont été déplacées ou ajoutées.
    
## <a name="remarks"></a>Remarques

Les propriétés transmises à **HrAddColumnsEx** à l’aide du paramètre _lpproptagColumnsNew_ deviennent les premières propriétés exposées lors des appels ultérieurs à la méthode [IMAPITable::QueryRows.](imapitable-queryrows.md) Toutes les propriétés précédemment dans le tableau qui n’ont pas été spécifiées dans le  _paramètre lpproptagColumnsNew_ sont exposées après toutes les propriétés ajoutées et déplacées. 
  
Si des propriétés de table ne sont pas définies lors de l’appel de **QueryRows,** elles sont renvoyées avec le type de propriété PT_NULL et l’identificateur de PROP_ID_NULL. 
  
## <a name="notes-to-callers"></a>Remarques pour les appelants

La fonction **HrAddColumnsEx** permet à l’appelant de fournir une fonction de rappel pour filtrer les colonnes déjà dans le tableau, par exemple pour convertir des chaînes du type de propriété PT_UNICODE en PT_STRING8. **HrAddColumnsEx** passe un pointeur vers le jeu de colonnes existant précédemment en tant que paramètre de la fonction de rappel. La fonction de rappel peut modifier les données dans le tableau de balises de propriétés, mais ne peut pas ajouter de nouvelles balises. 
  
 **HrAddColumnsEx** appelle d’abord la fonction de rappel s’il en existe une, ajoute ou déplace les colonnes spécifiées, puis appelle [IMAPITable::SetColumns](imapitable-setcolumns.md). 
  
Les paramètres d’entrée _lpAllocateBuffer_ et _lpFreeBuffer_ pointent respectivement vers les fonctions [MAPIAllocateBuffer](mapiallocatebuffer.md) et [MAPIFreeBuffer.](mapifreebuffer.md) Les valeurs exactes des pointeurs transmis à **HrAddColumnsEx** varient selon que l’appelant est une application cliente ou un fournisseur de services. Un client transmet des pointeurs vers les fonctions MAPI avec les noms spécifiés. Un fournisseur de services transmet les pointeurs qu’il a reçus dans son appel d’initialisation ou récupérés en appelant la méthode [IMAPISupport::GetMemAllocRoutines.](imapisupport-getmemallocroutines.md) 
  
## <a name="see-also"></a>Voir aussi



[IMAPITable::QueryColumns](imapitable-querycolumns.md)

