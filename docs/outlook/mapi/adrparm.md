---
title: ADRPARM
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ADRPARM
api_type:
- COM
ms.assetid: 35cd57b4-9901-456c-bf06-1f84e274eb4e
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 9663a25a50d914f47cff48124898d16318bbbc43
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425896"
---
# <a name="adrparm"></a>ADRPARM

**S’applique à** : Outlook 2013 | Outlook 2016 
  
Décrit l’affichage et le comportement de la boîte de dialogue d’adresse commune. 
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapidefs.h  <br/> |
   
```cpp
typedef struct _ADRPARM
{
  ULONG cbABContEntryID;
  LPENTRYID lpABContEntryID;
  ULONG ulFlags;
  LPVOID lpReserved;
  ULONG ulHelpContext;
  LPSTR lpszHelpFileName;
  LPFNABSDI lpfnABSDI;
  LPFNDISMISS lpfnDismiss;
  LPVOID lpvDismissContext;
  LPSTR lpszCaption;
  LPSTR lpszNewEntryTitle;
  LPSTR lpszDestWellsTitle;
  ULONG cDestFields;
  ULONG nDestFieldFocus;
  LPSTR FAR *lppszDestTitles;
  ULONG FAR *lpulDestComps;
  LPSRestriction lpContRestriction;
  LPSRestriction lpHierRestriction;
} ADRPARM, FAR *LPADRPARM;

```

## <a name="members"></a>Members

**cbABContEntryID**
  
> Nombre d’octets dans l’identificateur d’entrée pointé par **lpABContEntryID**.
    
**lpABContEntryID**
  
> Pointeur vers l’identificateur d’entrée du conteneur qui fournit la liste initiale des adresses des destinataires affichées dans la boîte de dialogue d’adresses.
    
**ulFlags**
  
> Masque de bits d’indicateurs associés à différentes options de boîte de dialogue d’adresses. Les indicateurs suivants peuvent être définies :
    
AB_RESOLVE
  
> Activez la résolution de tous les noms après la fermeture de la boîte de dialogue d’adresses. S’il existe des entrées ambiguës résultant du processus de résolution de noms, une boîte de dialogue s’affiche pour inviter l’utilisateur à les résoudre. La définition de cet indicateur garantit que tous les noms renvoyés par [IAddrBook::Address](iaddrbook-address.md) sont résolus. 
    
AB_SELECTONLY
  
> Désactivez la création d’adresses unique pour une liste de destinataires. Cet indicateur est utilisé uniquement si la boîte de dialogue est modale, comme indiqué par l’DIALOG_MODAL en cours de mise en place.
    
ADDRESS_ONE
  
> L’utilisateur peut sélectionner exactement un destinataire au lieu de plusieurs destinataires dans une liste. Cet indicateur n’est valide que lorsque **cDestFields** est zéro et que la boîte de dialogue est modale, comme indiqué par l’indicateur DIALOG_MODAL est définie. 
    
DIALOG_MODAL
  
> Entraîne l’affichage de la version modale de la boîte de dialogue d’adresse commune. Cet indicateur ou cet DIALOG_SDI doit être définie ; Ils ne peuvent pas être tous les deux définies. 
    
DIALOG_OPTIONS
  
> Entraîne **l’affichage du** bouton Options d’envoi dans la boîte de dialogue. Cet indicateur est utilisé uniquement si la boîte de dialogue est modale, comme indiqué par l’DIALOG_MODAL en cours de mise en place. 
    
DIALOG_SDI
  
> Entraîne l’affichage de la version non modée de la boîte de dialogue d’adresse commune. Cet indicateur ou cet DIALOG_MODAL doit être définie ; Ils ne peuvent pas être tous les deux définies. L DIALOG_SDI est ignoré pour les clients autres qu’Outlook et la version modale de la boîte de dialogue s’affiche. Par conséquent, un pointeur vers un handle ne doit pas être attendu dans le paramètre  _lpulUIParam_ de [IAddrBook::Address](iaddrbook-address.md).
    
**lpReserved**
  
> Réservé, doit être zéro.
    
**ulHelpContext**
  
> Spécifie le contexte  dans l’aide qui s’affiche pour la première fois lorsque l’utilisateur clique sur le bouton Aide dans la boîte de dialogue Adresse. 
    
**lpszHelpFileName**
  
> Pointeur vers le nom d’un fichier d’aide qui sera associé à la boîte de dialogue d’adresses. Le **membre lpszHelpFileName** est utilisé avec **ulHelpContext** pour appeler la fonction Windows **WinHelp.** 
    
**lpfnABSDI**
  
> Pointeur vers une fonction MAPI basée sur le prototype [ACCELERATEABSDI](accelerateabsdi.md) ou NULL. Ce membre s’applique uniquement à la version sans mode de la boîte de dialogue, comme indiqué par l’DIALOG_SDI en cours de mise en place. Les clients qui construisent une structure **ADRPARM** à transmettre à [IAddrBook::Address](iaddrbook-address.md) doivent toujours définir le membre **lpfnABSDI** sur NULL. Si l DIALOG_SDI est définie, MAPI le définira sur une fonction valide avant de le renvoyer. Les clients appellent cette fonction à partir de leur boucle de message pour s’assurer que les accélérateurs de la boîte de dialogue du carnet d’adresses fonctionnent. Lorsque la boîte de dialogue est fermée et que MAPI appelle la fonction pointée par le membre **lpfnDismiss,** les clients doivent déhooker la fonction **ACCELERATEABSDI** de leur boucle de messages. 
    
**lpfnDismiss**
  
> Pointeur vers une fonction basée sur le prototype [DISMISSMODELESS](dismissmodeless.md) ou NULL. Ce membre s’applique uniquement à la version sans mode de la boîte de dialogue, comme indiqué par l’indicateur DIALOG_SDI en cours de mise en place. MAPI appelle la **fonction DISMISSMODELESS** lorsque l’utilisateur fait disparaître la boîte de dialogue d’adresses sans mode, informant un client appelant **IAddrBook::Address** que la boîte de dialogue n’est plus active. 
    
**lpvDismissContext**
  
> Pointeur vers les informations de contexte à passer à la **fonction DISMISSMODELESS** pointée par le membre **lpfnDismiss.** Ce membre s’applique uniquement à la version sans mode de la boîte de dialogue, comme indiqué par l’indicateur DIALOG_SDI en cours de mise en place. 
    
**lpszCaption**
  
> Pointeur vers le texte à utiliser comme titre pour la boîte de dialogue Adresse commune.
    
**lpszNewEntryTitle**
  
> Pointeur vers le texte à utiliser comme étiquette de  bouton pour le bouton qui appelle la boîte de dialogue Nouvelle entrée ou une autre boîte de dialogue. 
    
**lpszDestWellsTitle**
  
> Pointeur vers le texte à utiliser comme titre pour les contrôles de zone de texte du destinataire qui peuvent apparaître dans la version modale de la boîte de dialogue Adresse commune. Ce membre n’est pas utilisé pour les boîtes de dialogue sans mode. 
    
**cDestFields**
  
> Nombre de contrôles de zone de texte de destinataire dans la version modale de la boîte de dialogue d’adresse, ou zéro si la boîte de dialogue est sans mode. La boîte de dialogue d’adresse est ouverte pour la navigation uniquement lorsque les conditions suivantes sont vraies : 
    
  - Le **membre cDestFields** est définie sur zéro. 
    
  - L DIALOG_BOX est définie.
    
  - L ADDRESS_ONE n’est pas définie.
    
  Définir **cDestFields** sur 0XFFFFFFFF signifie que MAPI doit créer le nombre par défaut de contrôles de zone de texte de destinataire. Dans ce cas, les **membres lppszDestTitles** et **lpulDestComps** doivent être NULL. 
    
**nDestFieldFocus**
  
> Indique le contrôle de zone de texte particulier qui doit avoir le focus initial lorsque la version modale de la boîte de dialogue s’affiche. Cette valeur doit être entre 0 et la valeur **de cDestFields** moins 1. 
    
**lppszDestTitles**
  
> Pointeur vers un tableau d’étiquettes pour les boutons associés à chacun des contrôles de zone de texte qui sont affichés dans la version modale de la boîte de dialogue d’adresse. La valeur du **membre cDestFields** indique le nombre d’étiquettes incluses dans le tableau. Si le **membre lppszDestTitles** est NULL, la méthode **Address** utilise les titres par défaut. 
    
**lpulDestComps**
  
> Pointeur vers un tableau de valeurs de type de destinataire, telles que MAPI_TO, MAPI_CC et MAPI_BCC, qui est associé à chaque contrôle de zone de texte. La valeur du **membre CDestFields** indique le nombre de types de destinataires inclus dans le tableau. Les valeurs pointées par **lpulDestComps** peuvent être utilisées pour définir la propriété **PR_RECIPIENT_TYPE** ([PidTagRecipientType](pidtagrecipienttype-canonical-property.md)) de chaque destinataire. Si le **membre lpulDestComps** est NULL, la méthode **Address** utilise les types de destinataires par défaut. 
    
**lpContRestriction**
  
> Pointeur vers une structure [SRestriction](srestriction.md) qui limite le type d’entrées d’adresse qui peuvent être affichées dans la boîte de dialogue. 
    
**lpHierRestriction**
  
> Pointeur vers une structure **SRestriction** qui limite les conteneurs de carnet d’adresses qui peuvent fournir des entrées d’adresse à afficher dans la boîte de dialogue. 
    
## <a name="remarks"></a>Remarques

Les structures **ADRPARM** sont utilisées par les clients et les fournisseurs de services pour contrôler l’apparence et le comportement des boîtes de dialogue d’adresse commune MAPI. Il existe deux variantes de la boîte de dialogue d’adresse : modeless et modal. Certains des membres de la structure **ADRPARM** s’appliquent aux deux versions de la boîte de dialogue, mais d’autres s’appliquent uniquement à l’une des deux versions. Le tableau suivant relie les membres d’une structure **ADRPARM** à leur utilisation avec les boîtes de dialogue d’adresses communes. 
  
|Membre ADRPARM|Type de boîte de dialogue|
|:-----|:-----|
|**cbABContEntryID** et **lpABContEntryID** <br/> |Modal et non modal  <br/> |
|**ulFlags** <br/> |Modal et non modal  <br/> |
|**lpReserved** <br/> |Modal et non modal  <br/> |
|**ulHelpContext** et **lpszHelpFileName** <br/> |Modal et non modal  <br/> |
|**lpfnABSDI** <br/> |Modeless  <br/> |
|**lpfnDismiss** et **lpvDismissContext** <br/> |Modeless  <br/> |
|**lpszCaption** <br/> |Modal et non modal  <br/> |
|**lpszNewEntryTitle** <br/> |Modal  <br/> |
|**lpszDestWellsTitle**, **cDestFields**, **nDestFieldFocus**, **lppszDestTitles** et **lpulDestComps** <br/> |Modal  <br/> |
|**lpContRestriction** <br/> |Modal et non modal  <br/> |
|**lpHierRestriction** <br/> |Modal et non modal  <br/> |
   
La boîte de dialogue sans mode est un affichage en lecture seule des entrées d’un ou plusieurs conteneurs de carnet d’adresses. La boîte de dialogue peut afficher toutes les entrées des conteneurs sélectionnés ou être limitée uniquement aux entrées et conteneurs qui correspondent aux critères établis par une restriction. La restriction de contenu pointée par **lpContRestriction** peut limiter les types d’entrées affichées et la restriction de hiérarchie pointée par **lpHierRestriction** peut limiter les conteneurs fournissant les entrées. Pour informer l’appelant lorsque la boîte de dialogue est rejetée, MAPI appelle une fonction fournie par l’appelant qui correspond au prototype [DISMISSMODELESS.](dismissmodeless.md) Une autre fonction, qui correspond au prototype [ACCELERATEABSDI,](accelerateabsdi.md) est fournie par MAPI et invoquée par l’appelant dans la boucle de message Windows pour faciliter le fonctionnement des raccourcis clavier. La version sans mode de la boîte de dialogue d’adresse MAPI peut être affichée lorsque les clients appellent [IAddrBook::Address](iaddrbook-address.md) ou lorsque les fournisseurs de services appellent [IMAPISupport::Address](imapisupport-address.md). 
  
La boîte de dialogue modale est un affichage en lecture/écriture des entrées d’un ou plusieurs conteneurs. Son contenu peut être affecté de la même manière que la version sans mode par des restrictions définies dans les membres **lpContRestriction** et **lpHierRestriction.** Outre la zone de liste affichant les entrées de conteneur, la boîte de dialogue modale peut contenir entre un et trois contrôles de zone de texte pour contenir les entrées sélectionnées par l’utilisateur. Chaque contrôle d’édition est associé à un type de destinataire ou **à une propriété PR_RECIPIENT_TYPE** spécifique, telle que MAPI_TO. La boîte de dialogue d’adresse modale peut être affichée par l’une des méthodes **Address** ou lorsque les clients appellent [IAddrBook::D etails](iaddrbook-details.md) et que les fournisseurs de services appellent [IMAPISupport::D etails](imapisupport-details.md). 
  
Cette illustration comprend deux contrôles de zone de texte, car le membre **cDestFields** de la structure **ADRPARM** contrôlant l’affichage de cette boîte de dialogue est définie sur 2. Le premier contrôle a le focus initial, car le membre **nDestFieldFocus** est définie sur 0. 
  
Le **membre lpszNewEntryTitle** pointe vers le texte d’une étiquette de bouton qui, lorsqu’elle est sélectionnée, entraîne l’affichage d’une boîte de dialogue supplémentaire. En règle générale, comme illustré dans l’illustration de la boîte de dialogue modale, le bouton est intitulé **Nouveau** et la boîte de dialogue qui s’affiche répertorie tous les types d’adresses qui peuvent être créés par n’importe quel fournisseur de carnet d’adresses dans le profil. Les clients  affichent cette boîte de dialogue Nouvelle entrée en appelant [IAddrBook::NewEntry](iaddrbook-newentry.md) et en passant zéro pour le paramètre _cbEidNewEntryTpl_ et NULL pour le paramètre _lpEidNewEntryTpl_ lorsque l’utilisateur sélectionne le bouton. Les informations incluses dans cette boîte de dialogue proviennent du tableau MAPI one-off. 
  
Chaque entrée de cette boîte de dialogue est associée à un modèle pour entrer les données requises pour créer une adresse du type particulier. La plupart des fournisseurs de carnet d’adresses fournissent un modèle pour chaque type d’entrée d’adresse qu’ils peuvent créer. Lorsqu’un utilisateur effectue une sélection dans cette boîte de dialogue, MAPI affiche le modèle correspondant.
  
Les quatre bits les plus significatifs du membre **ulFlags** de la structure **ADRPARM** contiennent un numéro de version identifiant la version de la structure **ADRPARM.** La version actuelle est 0 (zéro) ou ADRPARM_HELP_CTX. L’implémentation actuelle de MAPI échoue pour toute version de la structure autre que zéro. 
  
Les versions futures de la structure peuvent être complètement différentes . il se peut qu’ils ne prisent pas en charge la structure version zéro. Les macros suivantes sont fournies pour extraire le numéro de version du membre **ulFlags** et pour le combiner avec les indicateurs définis : 
  
- **GET_ADRPARM_VERSION** (_ulFlags_) 
- **SET_ADRPARM_VERSION** (_ulFlags_, _ ulVersion _) 
- **ADRPARM_HELP_CTX**
  
## <a name="see-also"></a>Voir aussi

- [ACCELERATEABSDI](accelerateabsdi.md)
- [DISMISSMODELESS](dismissmodeless.md)
- [IAddrBook::Address](iaddrbook-address.md)
- [IMAPISupport::Address](imapisupport-address.md)
- [SRestriction](srestriction.md)
- [Structures MAPI](mapi-structures.md)

