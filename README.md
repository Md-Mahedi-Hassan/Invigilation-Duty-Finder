# Invigilation Duty Finder - Complete v34

This version keeps the working Version 33 roster, video background, campus-photo fallback, committee page, and guidelines page, but removes the Attendance Sheet Generator page.

Upload all files from this package directly to the GitHub repository root.

## Required background video

Upload your background video to the repository root with this exact filename:

```text
diu.mp4
```

If `diu.mp4` is missing, blocked, or fails to load on a visitor's device, the site automatically shows `diu-campus.jpg` as the background.

## Pages included

- `index.html` - faculty duty roster search by name or initial
- `guidelines.html` - examination guidelines and dynamic slot schedule from `duty-roster.pdf`
- `committee.html` - exam committee contact directory with committee member images

## Removed page

The Attendance Sheet Generator page has been removed from this version. The navigation bar no longer links to it, and the attendance generator files are not included.

## Required PDF filenames

```text
duty-roster.pdf
faculty-list.pdf
exam-committee.pdf
```

## Committee photos

Upload committee member images using the faculty initial as the filename, for example:

```text
MHS.jpg
AAK.png
MJZ.jpeg
```

The site tries root-level images and common folders such as `images/`, `img/`, `photos/`, `committee-photos/`, and `assets/images/`. It supports `jpg`, `jpeg`, `png`, `gif`, `webp`, `jfif`, and `gpeg`, including uppercase/lowercase variants.

## GitHub Pages setup

```text
Settings > Pages
Source: Deploy from a branch
Branch: main
Folder: / (root)
```

After replacing files, wait for GitHub Pages to finish deployment, then hard refresh with `Ctrl + Shift + R`.

## Version note

Version 34 keeps the Version 33 first-day Slot A roster parser fix and all background behavior, but removes the Attendance Sheet Generator page.


Version 35 note: Faculty avatar badges now use the actual initial from the roster/faculty list instead of generating initials from the name. For example, Mehedi Hasan (MHH) now shows MHH in the avatar badge, not MH.


Version 36 note: Public source/debug labels and source-PDF links were removed from the Duty Roster, Examination Guidelines, and Exam Committee pages. Functionality is unchanged.
