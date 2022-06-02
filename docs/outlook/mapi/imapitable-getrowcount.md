---
title: IMAPITableGetRowCount
description: Décrit la syntaxe, les paramètres et la valeur de retour d’IMAPITableGetRowCount, qui retourne le nombre total de lignes dans la table.
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPITable.GetRowCount
api_type:
- COM
ms.assetid: 44a12c92-7462-4acf-9520-5d4c2d7f1d47
ms.openlocfilehash: 52f3777f3f2134b01e7804f2985c6250e61fd77c
ms.sourcegitcommit: e2b79cc4469013a4b3705620a93aa70b88e6c996
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/02/2022
ms.locfileid: "65827841"
---
# <a name="imapitablegetrowcount"></a>IMAPITable::GetRowCount

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Retourne le nombre total de lignes dans la table. 
  
```cpp
HRESULT GetRowCount(
ULONG ulFlags,
ULONG FAR * lpulCount
);
```

## <a name="parameters"></a>Paramètres

 _ulFlags_
  
> Réservé; doit être égal à zéro.
    
 _lpulCount_
  
> [out] Pointeur vers le nombre de lignes dans la table.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> Le nombre de lignes a été retourné avec succès.
    
MAPI_E_BUSY 
  
> Une autre opération est en cours qui empêche le démarrage de l’opération de récupération du nombre de lignes. Soit l’opération en cours doit être autorisée à se terminer, soit elle doit être arrêtée.
    
MAPI_E_NO_SUPPORT 
  
> La table ne peut pas calculer le nombre de lignes.
    
MAPI_W_APPROX_COUNT 
  
> L’appel a réussi, mais un nombre approximatif de lignes a été retourné, car le nombre exact de lignes n’a pas pu être déterminé éventuellement en raison de contraintes de mémoire. Pour tester cet avertissement, utilisez la macro **HR_FAILED** . Consultez [Utilisation de macros pour la gestion des erreurs](using-macros-for-error-handling.md).
    
## <a name="remarks"></a>Remarques

La méthode **IMAPITable::GetRowCount** récupère le nombre total de lignes dans une table. 
  
## <a name="notes-to-implementers"></a>Remarques pour les responsables de l’implémentation

Si vous ne pouvez pas déterminer le nombre de lignes exact de la table, retournez MAPI_W_APPROX_COUNT et un nombre approximatif de lignes dans le contenu du paramètre  _lpulCount_ . 
  
## <a name="notes-to-callers"></a>Remarques pour les appelants

Utilisez **GetRowCount** pour déterminer le nombre de lignes qu’une table contient avant d’appeler la méthode [IMAPITable::QueryRows](imapitable-queryrows.md) pour récupérer les données. S’il y a moins de vingt lignes dans la table, il est sûr d’appeler **QueryPosition** pour récupérer la table entière. S’il y a plus de vingt lignes dans la table, envisagez d’effectuer plusieurs appels à **QueryPosition** et limitez le nombre de lignes récupérées dans chaque appel. 
  
Certaines tables ne prennent pas en charge **GetRowCount** et retournent MAPI_E_NO_SUPPORT. Si **GetRowCount** n’est pas pris en charge, vous pouvez également appeler [IMAPITable::QueryPosition](imapitable-queryposition.md). Avec les résultats de **QueryPosition**, vous pouvez déterminer la relation entre la ligne actuelle et la dernière ligne. 
  
Lorsque **GetRowCount** retourne MAPI_E_BUSY parce qu’il ne peut pas récupérer temporairement un nombre de lignes, appelez la méthode [IMAPITable::WaitForCompletion](imapitable-waitforcompletion.md) . Lorsque **WaitForCompletion** est retourné, réessayez l’appel à **GetRowCount**. Une autre façon de détecter si une opération asynchrone est en cours consiste à appeler la méthode [IMAPITable::GetStatus](imapitable-getstatus.md) et à vérifier le contenu du paramètre  _lpulTableState_ . 
  
## <a name="mfcmapi-reference"></a>Référence MFCMAPI

Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.
  
|**Fichier**|**Fonction**|**Commentaire**|
|:-----|:-----|:-----|
|MAPIFunctions.cpp  <br/> |CopyFolderContents  <br/> |MFCMAPI utilise la méthode **IMAPITable::GetRowCount** pour déterminer le nombre de lignes dans la table source afin que la mémoire puisse être allouée pour effectuer la copie. |
   
## <a name="see-also"></a>Voir aussi



[IMAPITable::GetStatus](imapitable-getstatus.md)
  
[IMAPITable::QueryPosition](imapitable-queryposition.md)
  
[IMAPITable::QueryRows](imapitable-queryrows.md)
  
[IMAPITable::WaitForCompletion](imapitable-waitforcompletion.md)
  
[IMAPITable : IUnknown](imapitableiunknown.md)


[MFCMAPI comme un exemple de Code](mfcmapi-as-a-code-sample.md)

