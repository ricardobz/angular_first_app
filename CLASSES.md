# Module 1 & 2

## Selectors


```javascript
selector: 'app-servers'
selector: '[app-servers]'
selector: '.app-servers'
```
Respectively:
```html
<app-servers></app-servers>
<div app-servers></div>
<div class="app-servers"></div>
```


## String interpolation
```html
<p>{{ title }}</p>
```

## Property binding

```html
<p [innerText]="title"></p>
```

## Event binding

```html
<input type="text" (input)="onUpdateServerName($event)"/>
<button (click)="onCreateServer()">
  Add server
</button>
```

## Two-way data binding

```html
<input type="text" [(ngModel)]="serverName"/>
```

## Directives (ngIf)

```html
<p *ngIf="serverCreated">Server was created! Name is {{ serverName }}</p>
```

## Directives (ngStyle)

```html
<p [ngStyle]="{ backgroundColor: getColor() }">
  Server with ID {{ serverId }} is {{ getServerStatus() }}!
</p>
```

## Directives (ngClass)
Class .online already declared in css file

```html
<p
  [ngClass]="{ online: serverStatus === 'online' }"
>
  Server with ID {{ serverId }} is {{ getServerStatus() }}!
</p>
```

## Directives (ngFor)

```html
<app-server *ngFor="let server of servers"></app-server>
```
