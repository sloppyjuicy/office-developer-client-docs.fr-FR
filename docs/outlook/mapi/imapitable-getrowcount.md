---
title: IMAPITableGetRowCount
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPITable.GetRowCount
api_type:
- COM
ms.assetid: 44a12c92-7462-4acf-9520-5d4c2d7f1d47
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 71178f1a531bd381387e0aa7fbacb02d4431a401
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22584323"
---
# <a name="imapitablegetrowcount"></a>IMAPITable::GetRowCount

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Renvoie le nombre total de lignes dans le tableau. 
  
```cpp
HRESULT GetRowCount(
ULONG ulFlags,
ULONG FAR * lpulCount
);
```

## <a name="parameters"></a>Param�tres

 _ulFlags_
  
> Réservé ; doit être égal à zéro.
    
 _lpulCount_
  
> [out] Pointeur vers le nombre de lignes dans le tableau.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> Le nombre de lignes a été renvoyé avec succès.
    
MAPI_E_BUSY 
  
> Une autre opération est en cours qui empêche l’opération de récupération de nombre de ligne de démarrer. L’opération en cours doit être autorisée à effectuer ou il doit être arrêté.
    
MAPI_E_NO_SUPPORT 
  
> Le tableau ne peut pas calculer le nombre de lignes.
    
MAPI_W_APPROX_COUNT 
  
> L’appel a réussi, mais un nombre de lignes approximatif a été renvoyé, car le nombre exact de lignes pas pu être déterminé éventuellement à cause de contraintes de mémoire. Pour tester cet avertissement, utilisez la macro **HR_FAILED** . Consultez [utilisation de Macros pour la gestion des erreurs](using-macros-for-error-handling.md).
    
## <a name="remarks"></a>Remarques

La méthode **IMAPITable::GetRowCount** récupère le nombre total de lignes dans un tableau. 
  
## <a name="notes-to-implementers"></a>Remarques à l’attention des responsables de l’implémentation

Si vous ne peut pas déterminer le nombre de lignes exact de la table, renvoyée MAPI_W_APPROX_COUNT et une ligne approximative count dans le contenu du paramètre _lpulCount_ . 
  
## <a name="notes-to-callers"></a>Notes aux appelants

Utilisez **GetRowCount** pour déterminer le nombre de lignes un tableau contient avant d’effectuer un appel à la méthode [IMAPITable::QueryRows](imapitable-queryrows.md) pour récupérer les données. S’il y a moins de 20 lignes dans le tableau, il est recommandé d’appeler **QueryPosition** pour récupérer l’ensemble du tableau. S’il y a plus de 20 lignes dans le tableau, envisagez de faire plusieurs appels **QueryPosition** et limiter le nombre de lignes récupérées dans chaque appel. 
  
Certaines tables ne pas prendre en charge **GetRowCount** et retourner MAPI_E_NO_SUPPORT. Si **GetRowCount** n’est pas pris en charge, une alternative peut être pour appeler [IMAPITable::QueryPosition](imapitable-queryposition.md). Avec les résultats du **QueryPosition**, vous pouvez déterminer la relation entre la ligne actuelle et la dernière ligne. 
  
**GetRowCount** retourne MAPI_E_BUSY, car il est temporairement Impossible d’extraire un nombre de lignes, appelez la méthode [IMAPITable::WaitForCompletion](imapitable-waitforcompletion.md) . Lorsque **WaitForCompletion** renvoie, réessayez l’appel vers **GetRowCount**. Une autre façon de détecter si une opération asynchrone est en cours consiste à appeler la méthode [IMAPITable::GetStatus](imapitable-getstatus.md) et vérifiez le contenu du paramètre _lpulTableState_ . 
  
## <a name="mfcmapi-reference"></a>Référence MFCMAPI

Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.
  
|**Fichier**|**Fonction**|**Commentaire**|
|:-----|:-----|:-----|
|MAPIFunctions.cpp  <br/> |CopyFolderContents  <br/> |MFCMAPI utilise la méthode **IMAPITable::GetRowCount** pour déterminer le nombre de lignes dans la table source afin de mémoire pouvant être allouée pour effectuer la copie.  <br/> |
   
## <a name="see-also"></a>Voir aussi



[IMAPITable::GetStatus](imapitable-getstatus.md)
  
[IMAPITable::QueryPosition](imapitable-queryposition.md)
  
[IMAPITable::QueryRows](imapitable-queryrows.md)
  
[IMAPITable::WaitForCompletion](imapitable-waitforcompletion.md)
  
[IMAPITable : IUnknown](imapitableiunknown.md)


[MFCMAPI comme un exemple de Code](mfcmapi-as-a-code-sample.md)

