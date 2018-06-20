---
title: HrCreateApptRebaser
manager: soliver
ms.date: 12/07/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 265028b7-a583-f6ba-0214-5a4322f98f35
description: Initialise un objet IOlkApptRebaser à utiliser lors de la redéfinition des rendez-vous dans les calendriers Outlook.
ms.openlocfilehash: fec0407c3f129290d03f9b26b0b3f072a229b003
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19782576"
---
# <a name="hrcreateapptrebaser"></a>HrCreateApptRebaser

Initialise un objet [IOlkApptRebaser](iolkapptrebaser.md) à utiliser lors de la redéfinition des rendez-vous dans les calendriers Outlook. 
  
## <a name="quick-info"></a>Informations rapides

|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |tzmovelib.h  <br/> |
|Implémentée par :  <br/> |tzmovelib.dll  <br/> |
|Appelée par :  <br/> |Applications clientes MAPI  <br/> |
|Type de pointeur :  <br/> |**LPHRCREATEAPPTREBASER** <br/> |
|Point d’entrée DLL :  <br/> |**HrCreateApptRebaser@44** <br/> |
   
```cpp
HRESULT HrCreateApptRebaser(  
    ULONG ulFlags, 
    IMAPISession *pSession, 
    IMsgStore *pCalendarMsgStore, 
    IMAPIFolder *pCalendarFolder, 
    LPCWSTR pwszUpdatePrefix, 
    const FILETIME *pftInstallDateUTC, 
    LONG lExpansionDepth, 
    const TZDEFINITION *pTZTo, 
    const TZDEFINITION *pTZMissing, 
    MAPIERROR **ppError, 
    IOlkApptRebaser **ppApptRebase); 

```

## <a name="parameters"></a>Param�tres

_ulFlags_
  
> [in] Obligatoire. Un masque binaire composé des indicateurs utilisés pour contrôler comment redéfinir est effectuée. Les indicateurs suivants peuvent être définies et sont définies dans tzmovelib.h :
    
   - **REBASE_FLAG_UPDATE_ORGANIZED_MEETINGS** : éléments de rendez-vous dans laquelle l’utilisateur est l’organisateur de la réunion sont redéfinies. Notez que par défaut, cela entraîne Outlook pour envoyer des mises à jour de réunion à tous les participants à une réunion en cours redéfinie. Vous pouvez combiner cet indicateur avec **REBASE_FLAG_FORCE_NO_EX_UPDATES** ou **REBASE_FLAG_FORCE_NO_UPDATES** pour modifier le mode de gestion des mises à jour de la réunion. 
    
   - **REBASE_FLAG_UPDATE_UNMARKED** : mettre à jour des éléments de rendez-vous qui n’ont pas été marqués avec un fuseau horaire. Si cet indicateur n’est spécifié, la valeur de *pTZMissing* est utilisée comme un élément est créé dans le fuseau horaire pour tous les éléments qui n’ont pas de données de fuseau horaire. 
    
   - **REBASE_FLAG_UPDATE_ONLYRECURRING** : mettre à jour uniquement les éléments de rendez-vous périodiques. 
    
   - **REBASE_FLAG_NO_UI** : ne pas afficher une interface utilisateur (IU), y compris les boîtes de dialogue d’ouverture de session sont généralement affichés lors de l’ouverture d’une banque de messages. 
    
   - **REBASE_FLAG_UPDATE_MINIMIZEAPPTS** : ne pas redéfinir des éléments de rendez-vous qui se produisent dans le passé. 
    
   - **REBASE_FLAG_FORCE_REBASE** : ne pas vérifier l’organisateur pour redéfinir des décisions, mais redéfinir les éléments de rendez-vous dans laquelle l’utilisateur est un participant. 
    
   - **REBASE_FLAG_FORCE_NO_EX_UPDATES** — envoyer des mises à jour uniquement si l’utilisateur est l’organisateur et le destinataire n’est pas connecté à un serveur Exchange. 
    
   - **REBASE_FLAG_FORCE_NO_UPDATES** : ne jamais envoyer des mises à jour. 
    
   - **REBASE_FLAG_ONLY_CREATED_PRE_PATCH** — redéfinir uniquement les éléments de rendez-vous uniques créés avant le correctif a été appliqué. 
    
   - **REBASE_FLAG_REPORTING_MODE** : ne pas réellement rebase, rapport uniquement les éléments de rendez-vous qui doit être redéfini. 
    
   - **REBASE_FLAG_SEND_RESOURCE_UPDATES** — envoie des mises à jour de réunion à des ressources. 
    
_pSession_
  
> [in] Obligatoire. Pointeur vers une interface de session MAPI.
    
_pCalendarMsgStore_
  
> [in] Obligatoire. Pointeur vers une banque de messages contenant des éléments de rendez-vous à être redéfini.
    
_pCalendarFolder_
  
> [in] Obligatoire. Pointeur vers un dossier de calendrier contenant des éléments de rendez-vous à être redéfini.
    
_pwszUpdatePrefix_
  
> [in] Facultatif. Pointeur vers une chaîne contenant le préfixe à sur les demandes de réunion. Peut être NULL.
    
_pftInstallDateUTC_
  
> [in] Facultatif. Date d’installation du correctif de fuseau horaire. Utilisé uniquement si l’indicateur **REBASE_FLAG_ONLY_CREATED_PRE_PATCH** est défini. 
    
_IExpansionDepth_
  
> [in] Facultatif. La profondeur d’extension lors de la distribution de développement des listes à exclure des destinataires connecté au serveur Exchange. Utilisé uniquement si l’indicateur **REBASE_FLAG_FORCE_NO_EX_UPDATES** est défini. 
    
_pTZTo_
  
> [in] Obligatoire. Pointeur vers une structure **TZDEFINITION** décrivant le fuseau horaire à être redéfini à. **TZDEFINITION** est défini dans tzmovelib. 
    
pTZMissing
  
> [in] Obligatoire. Pointeur vers une structure **TZDEFINITION** décrivant le fuseau horaire pour être déterminée automatiquement si les informations de fuseau horaire ne sont pas marquées sur un élément. Ne doit pas être NULL, mais uniquement si l’indicateur **REBASE_FLAG_UPDATE_UNMARKED** est défini. 
    
_ppError_
  
> [out] Pointeur vers un pointeur vers une structure **MAPIERROR** contenant des informations de version, composant et le contexte de l’erreur. Peut être NULL si aucune information d’erreur étendue n’est souhaitée. Gratuit avec [MAPIFreeBuffer](http://msdn.microsoft.com/library/9412594f-8acc-4c7e-a668-4ec1da0ad9cf%28Office.15%29.aspx). 
    
_ppApptRebase_
  
> [out] Pointeur vers un pointeur vers l’interface **IOlkApptRebaser** retournée. 
    
## <a name="return-values"></a>Valeurs de retour

S_OK si l'appel a réussi ; dans le cas contraire, un code d'erreur.
  
## <a name="remarks"></a>Note

Lorsque vous utilisez [GetProcAddress](http://msdn.microsoft.com/library/a0d7fc09-f888-4f46-a571-d3719a627597%28Office.15%29.aspx) pour rechercher l’adresse de cette fonction dans tzmovelib.dll, spécifiez **HrCreateApptRebaser@44** comme nom de la procédure. Tous les indicateurs sont valides en combinaison avec eux. 
  
Pour plus d’informations sur les différentes options, voir la section « Glossaire des options de ligne de commande pour l’outil de mise à jour des données de fuseau horaire Outlook » dans [931667 de la base de connaissances : comment faire pour résoudre les modifications de fuseau horaire à l’aide de l’outil de mise à jour de données de fuseau horaire pour Microsoft Office Outlook](http://support.microsoft.com/kb/931667/en-us).
  
## <a name="see-also"></a>Voir aussi

- [À propos de la relocalisation des calendriers par programme à l'heure](about-rebasing-calendars-programmatically-for-daylight-saving-time.md)

