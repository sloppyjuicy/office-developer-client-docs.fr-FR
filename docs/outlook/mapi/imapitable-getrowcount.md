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
  
> MSR doit être égal à zéro.
    
 _lpulCount_
  
> remarquer Pointeur vers le nombre de lignes dans le tableau.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> Le nombre de lignes a été correctement renvoyé.
    
MAPI_E_BUSY 
  
> Une autre opération est en cours, ce qui empêche le démarrage de l'opération de récupération du nombre de lignes. L'opération en cours doit être autorisée ou elle doit être arrêtée.
    
MAPI_E_NO_SUPPORT 
  
> Le tableau ne peut pas calculer le nombre de lignes.
    
MAPI_W_APPROX_COUNT 
  
> L'appel a réussi, mais un nombre approximatif de lignes a été renvoyé, car le nombre exact de lignes n'a pas pu être déterminé en raison de contraintes de mémoire. Pour tester cet avertissement, utilisez la macro **HR_FAILED** . Consultez la rubrique [utilisation des macros pour la gestion des erreurs](using-macros-for-error-handling.md).
    
## <a name="remarks"></a>Remarques

La méthode **IMAPITable:: GetRowCount** récupère le nombre total de lignes dans un tableau. 
  
## <a name="notes-to-implementers"></a>Remarques pour les responsables de l’implémentation

Si vous ne pouvez pas déterminer le nombre exact de lignes de la table, renvoyez MAPI_W_APPROX_COUNT et un nombre approximatif de lignes dans le contenu du paramètre _lpulCount_ . 
  
## <a name="notes-to-callers"></a>Remarques pour les appelants

Utilisez **GetRowCount** pour déterminer le nombre de lignes qu'une table contient avant d'appeler la méthode [IMAPITable:: QueryRows](imapitable-queryrows.md) pour extraire les données. S'il y a moins de vingt lignes dans le tableau, il est possible d'appeler **QueryPosition** pour récupérer le tableau entier. S'il y a plus de vingt lignes dans le tableau, envisagez d'effectuer plusieurs appels à **QueryPosition** et limitez le nombre de lignes extraites dans chaque appel. 
  
Certaines tables ne prennent pas en charge **GetRowCount** et renvoient MAPI_E_NO_SUPPORT. Si **GetRowCount** n'est pas pris en charge, vous pouvez également appeler la méthode [IMAPITable:: QueryPosition](imapitable-queryposition.md). Avec les résultats d' **QueryPosition**, vous pouvez déterminer la relation entre la ligne active et la dernière ligne. 
  
Lorsque **GetRowCount** renvoie MAPI_E_BUSY parce qu'il est temporairement incapable de récupérer un nombre de lignes, appelez la méthode [IMAPITable:: WaitForCompletion](imapitable-waitforcompletion.md) . Lorsque **WaitForCompletion** renvoie, essayez à nouveau l'appel à **GetRowCount**. Pour détecter si une opération asynchrone est en cours, vous pouvez également appeler la méthode [IMAPITable:: GetStatus](imapitable-getstatus.md) et vérifier le contenu du paramètre _lpulTableState_ . 
  
## <a name="mfcmapi-reference"></a>Référence MFCMAPI

Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.
  
|**Fichier**|**Fonction**|**Commentaire**|
|:-----|:-----|:-----|
|MAPIFunctions. cpp  <br/> |CopyFolderContents  <br/> |MFCMAPI utilise la méthode **IMAPITable:: GetRowCount** pour déterminer le nombre de lignes contenues dans la table source de sorte que la mémoire puisse être allouée à l'exécution de la copie.  <br/> |
   
## <a name="see-also"></a>Voir aussi



[IMAPITable::GetStatus](imapitable-getstatus.md)
  
[IMAPITable::QueryPosition](imapitable-queryposition.md)
  
[IMAPITable::QueryRows](imapitable-queryrows.md)
  
[IMAPITable::WaitForCompletion](imapitable-waitforcompletion.md)
  
[IMAPITable : IUnknown](imapitableiunknown.md)


[MFCMAPI comme un exemple de Code](mfcmapi-as-a-code-sample.md)

