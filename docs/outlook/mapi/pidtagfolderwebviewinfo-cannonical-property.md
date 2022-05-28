---
title: Propriété canonique PidTagFolderWebViewInfo
description: Décrit la propriété canonique PidTagFolderWebViewInfo, qui contient l’URL de la page d’accueil d’un dossier dans Microsoft Outlook.
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- PidTagFolderWebViewInfo
api_type:
- HeaderDef
ms.assetid: 96ea23df-aa4f-4b3e-9663-e7db39f668c1
ms.openlocfilehash: 71f9b8bd36d4e0d06ae650444b93d952e8d16cd0
ms.sourcegitcommit: 8c8e4ac05a6612dd5c815ab18ba40e56a6ba839d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/28/2022
ms.locfileid: "65770669"
---
# <a name="pidtagfolderwebviewinfo-cannonical-property"></a>Propriété canonique PidTagFolderWebViewInfo

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient l’URL de la page d’accueil d’un dossier dans Microsoft Outlook. Cette propriété contient un flux binaire appelé **WebViewPersistenceObject**.
  
|Propriété |Valeur |
|:-----|:-----|
|Propriétés associées :  <br/> |PR_FOLDER_WEBVIEWINFO  <br/> |
|Identificateur :  <br/> |0x36DF  <br/> |
|Type de données :  <br/> |PT_BINARY  <br/> |
|Domaine :  <br/> |Dossier MAPI  <br/> |
   
## <a name="remarks"></a>Remarques

Une URL de page d’accueil peut être spécifiée pour n’importe quel dossier Outlook. Ces informations sont accessibles dans Outlook à partir de l’onglet **Page d’accueil** de la boîte de dialogue Propriétés d’un dossier. 
  
Selon certains paramètres de stratégie, la page d’accueil peut être ignorée par Outlook si le magasin MAPI qui contient ce dossier ne signale pas MSCAP_SECURE_FOLDER_HOMEPAGES dans son implémentation [IMSCapabilities::GetCapabilities](pidtagfolderwebviewinfo-cannonical-property.md). 
  
Le dossier **Outlook Aujourd’hui** et un dossier public peuvent avoir des URL de page d’accueil. Toutefois, le dossier **Outlook Today** utilise un autre mécanisme pour gérer son URL de page d’accueil ; ce mécanisme n’est pas abordé dans cette rubrique. Un dossier public peut également avoir une URL de page d’accueil définie dans celui-ci qui est spécifique à un utilisateur. Toutefois, cette fonctionnalité n’est pas décrite dans cette rubrique. 
  
La valeur de cette propriété est un flux binaire appelé **WebViewPersistenceObject**.
  
### <a name="webviewpersistenceobject-stream-structure"></a>Structure de flux WebViewPersistenceObject

La structure de flux **WebViewPersistenceObject** contient des informations sur une URL de page d’accueil pour un dossier. 
  
Les éléments de données de cette structure sont stockés dans un ordre d’octets little-endian, immédiatement après l’autre dans l’ordre spécifié suivant. 
  
> [!NOTE]
> La description suivante peut ne pas répertorier toutes les valeurs de champ prises en charge par Outlook. Par conséquent, lorsque votre code lit un flux existant, certains indicateurs qui ne sont pas répertoriés ici peuvent également être trouvés. Toutefois, vous pouvez utiliser cette description pour créer par programmation des valeurs pour la propriété **PidTagFolderWebViewInfo** que Outlook comprendreez. 
  
 _dwVersion_
  
> DWORD (4 octets). Version du format de la structure. Depuis Microsoft Office Outlook 2007, la seule valeur prise en charge pour ce champ est la suivante.
    
|**Nom de la valeur**|**Valeur**|
|:-----|:-----|
|WEBVIEW_PERSISTENCE_VERSION  <br/> |0x00000002  <br/> |
   
 _dwType_
  
> DWORD (4 octets). Type des informations de la page d’accueil. Depuis Microsoft Office Outlook 2007, la seule valeur prise en charge pour ce champ est la suivante.
    
|**Nom de la valeur**|**Valeur**|
|:-----|:-----|
|WEBVIEWURL  <br/> |0x00000001  <br/> |
   
 _dwFlags_
  
> DWORD (4 octets). Combinaison de zéro ou plusieurs indicateurs dont les valeurs et significations sont répertoriées dans le tableau suivant.
    
|Nom de l’indicateur****|****Valeur****|****Description****|
|:-----|:-----|:-----|
|WEBVIEW_FLAGS_SHOWBYDEFAULT  <br/> |0x00000001  <br/> |La **case à cocher Afficher la page d’accueil par défaut pour ce dossier** a été cochée sous l’onglet **Page d’accueil** de la boîte de dialogue Propriétés d’un dossier. |
   
 _dwUnused[7]_
  
> Tableau de 7 éléments DWORD (28 octets au total). Inutilisés.
    
cbData
  
> ULONG (4 octets). Taille, en octets, de l’élément de données  _wzURL_ . 
    
 _wzURL_
  
> Tableau d’éléments WCHAR. Représentation UTF-16 de la chaîne d’URL de la page d’accueil sans fin.
    
### <a name="webviewpersistenceobject-stream-sample"></a>Exemple de flux WebViewPersistenceObject

Cette section décrit un exemple de flux **WebViewPersistenceObject** . Le flux spécifie l’URL de la page d’accueil «https://www.microsoft.com ». 
  
 **Vidage des données**
  
Voici un vidage de données du flux tel qu’il serait affiché dans un éditeur binaire.
  
|**Décalage de flux**|**Octets de données**|**Données ASCII**|
|:-----|:-----|:-----|
|0000000000  <br/> | `02 00 00 00 01 00 00 00 01 00 00 00 00 00 00 00` <br/> | `?...?...?.......` <br/> |
|0000000010  <br/> | `00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00` <br/> | `................` <br/> |
|0000000020  <br/> | `00 00 00 00 00 00 00 00 32 00 00 00 68 00 74 00` <br/> | `........2...h.t.` <br/> |
|0000000030  <br/> | `74 00 70 00 3A 00 2F 00 2F 00 77 00 77 00 77 00` <br/> | `t.p.:././.w.w.w.` <br/> |
|0000000040  <br/> | `2E 00 6D 00 69 00 63 00 72 00 6F 00 73 00 6F 00` <br/> | `..m.i.c.r.o.s.o.` <br/> |
|0000000050  <br/> | `66 00 74 00 2E 00 63 00 6F 00 6D 00 00 00` <br/> | `f.t...c.o.m...` <br/> |
   
Voici une analyse des exemples de données pour le flux **WebViewPersistenceObject** . 
  
 _dwVersion_
  
> Décalage 0x0, 4 octets : 0x00000002 (WEBVIEW_PERSISTENCE_VERSION).
    
 _dwType_
  
> Décalage 0x4, 4 octets : 0x00000001 (WEBVIEWURL).
    
 _dwFlags_
  
> Offset 0x8, 4 octets : 0x00000001 (WEBVIEW_FLAGS_SHOWBYDEFAULT).
    
 _dwUnused[7]_
  
> Décalage 0xC, 28 octets : tous les zéros.
    
 _cbData_
  
> Offset 0x28, 4 octets : 0x00000032.
    
 _wzURL_
  
> Offset 0x2C, 0x32 octets : tableau de 25 WCHAR. Valeur de chaîne sans fin Unicode : «https://www.microsoft.com ».
    

