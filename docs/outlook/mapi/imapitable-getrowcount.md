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
ms.openlocfilehash: b13bf3bdd8392efc42ad189e48dffad8636f0708
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425602"
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

## <a name="parameters"></a>Paramètres

 _ulFlags_
  
> Réservé ; doit être zéro.
    
 _lpulCount_
  
> [out] Pointeur vers le nombre de lignes du tableau.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> Le nombre de lignes a été renvoyé avec succès.
    
MAPI_E_BUSY 
  
> Une autre opération est en cours qui empêche le démarrage de l’opération de récupération du nombre de lignes. L’opération en cours doit être autorisée ou arrêtée.
    
MAPI_E_NO_SUPPORT 
  
> Le tableau ne peut pas calculer le nombre de lignes.
    
MAPI_W_APPROX_COUNT 
  
> L’appel a réussi, mais un nombre approximatif de lignes a été renvoyé, car le nombre exact de lignes n’a pas pu être déterminé en raison de contraintes de mémoire. Pour tester cet avertissement, utilisez la macro **HR_FAILED.** Voir [Utilisation de macros pour la gestion des erreurs.](using-macros-for-error-handling.md)
    
## <a name="remarks"></a>Remarques

La **méthode IMAPITable::GetRowCount** récupère le nombre total de lignes dans un tableau. 
  
## <a name="notes-to-implementers"></a>Remarques pour les responsables de l’implémentation

Si vous ne pouvez pas déterminer le nombre exact de lignes du tableau, renvoyez MAPI_W_APPROX_COUNT nombre de lignes et un nombre approximatif de lignes dans le contenu du _paramètre lpulCount._ 
  
## <a name="notes-to-callers"></a>Remarques pour les appelants

Utilisez **GetRowCount pour** connaître le nombre de lignes qu’une table contient avant d’appeler la méthode [IMAPITable::QueryRows](imapitable-queryrows.md) pour récupérer les données. S’il y a moins de vingt lignes dans la table, il est sûr d’appeler **QueryPosition** pour récupérer la table entière. Si la table compte plus de vingt lignes, envisagez d’effectuer plusieurs appels à **QueryPosition** et limitez le nombre de lignes récupérées dans chaque appel. 
  
Certaines tables ne peuvent pas prendre **en charge GetRowCount** et renvoyer des MAPI_E_NO_SUPPORT. Si **GetRowCount n’est** pas pris en charge, une alternative peut être d’appeler [IMAPITable::QueryPosition](imapitable-queryposition.md). Avec les résultats **de QueryPosition,** vous pouvez déterminer la relation entre la ligne actuelle et la dernière ligne. 
  
Lorsque **GetRowCount renvoie** MAPI_E_BUSY car il est temporairement incapable de récupérer un nombre de lignes, appelez la méthode [IMAPITable::WaitForCompletion.](imapitable-waitforcompletion.md) Lorsque **WaitForCompletion est** de retour, réessayez l’appel **à GetRowCount**. Une autre façon de détecter si une opération asynchrone est en cours consiste à appeler la méthode [IMAPITable::GetStatus](imapitable-getstatus.md) et à vérifier le contenu du paramètre _lpulTableState._ 
  
## <a name="mfcmapi-reference"></a>Référence MFCMAPI

Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.
  
|**Fichier**|**Fonction**|**Commentaire**|
|:-----|:-----|:-----|
|MAPIFunctions.cpp  <br/> |CopyFolderContents  <br/> |MFCMAPI utilise la méthode **IMAPITable::GetRowCount** pour déterminer le nombre de lignes dans la table source afin que la mémoire puisse être allouée pour effectuer la copie.  <br/> |
   
## <a name="see-also"></a>Voir aussi



[IMAPITable::GetStatus](imapitable-getstatus.md)
  
[IMAPITable::QueryPosition](imapitable-queryposition.md)
  
[IMAPITable::QueryRows](imapitable-queryrows.md)
  
[IMAPITable::WaitForCompletion](imapitable-waitforcompletion.md)
  
[IMAPITable : IUnknown](imapitableiunknown.md)


[MFCMAPI comme un exemple de Code](mfcmapi-as-a-code-sample.md)

